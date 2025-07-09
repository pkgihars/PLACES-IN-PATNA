<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Discover Patna – 1000+ Places</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    /* 🧩 Same styles as before with max-width adjustments */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: 'Inter', sans-serif; background: #f9f9f9; color: #333; }
    header { background: linear-gradient(to right, #005f73, #0a9396); color: white; text-align: center; padding: 60px 20px; }
    header h1 { font-size: 3em; margin-bottom: 10px; }
    header p { font-size: 1.2em; opacity: 0.9; }
    .search-bar { max-width: 600px; margin: 30px auto; display: flex; align-items: center; padding: 8px 16px; background: white; border-radius: 12px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
    .search-bar input { width: 100%; border: none; font-size: 16px; padding: 10px; outline: none; }
    .container { max-width: 1000px; margin: auto; padding: 20px; display: flex; flex-direction: column; gap: 30px; align-items: center; }
    .place { background: white; width: 100%; max-width: 700px; border-radius: 16px; overflow: hidden; box-shadow: 0 8px 20px rgba(0,0,0,0.06); transition: transform 0.3s ease; }
    .place:hover { transform: translateY(-5px); }
    .place img { width: 100%; height: auto; }
    .place-content { padding: 20px; }
    .place-content h2 { color: #0a9396; font-size: 1.5em; margin-bottom: 8px; }
    .short-desc { font-style: italic; color: #777; margin-bottom: 10px; }
    .place-content p { line-height: 1.6; }
    .map-button { display: inline-block; margin-top: 15px; background: #0a9396; color: white; padding: 10px 16px; text-decoration: none; border-radius: 8px; transition: background 0.3s; }
    .map-button:hover { background: #005f73; }
    .download-map, .contact { text-align: center; margin: 50px 0; }
    .download-map a, .contact a { padding: 14px 24px; background: #005f73; color: white; font-weight: 600; border-radius: 10px; text-decoration: none; font-size: 18px; transition: background 0.3s; }
    .download-map a:hover, .contact a:hover { background: #0a9396; }
    .contact a { background: #d6336c; }
    .contact a:hover { background: #ad2858; }
    @media (max-width: 768px) { header h1 { font-size: 2em; } .place-content h2 { font-size: 1.3em; } }
  </style>
</head>
<body>

  <header>
    <h1>🌆 Discover Patna – 1000+ Places</h1>
    <p>Explore every landmark, neighborhood & hidden gem</p>
  </header>

  <div class="search-bar">
    <input type="text" id="searchInput" placeholder="🔍 Search for any place..." onkeyup="searchPlaces()">
  </div>

  <div class="container" id="placesContainer">
    <!-- Cards will be generated here -->
  </div>

  <div class="download-map">
    <a href="https://www.google.com/maps/d/u/0/viewer?mid=1XTVrAsaOIhTXaKrqZ3apKqHdZOE&hl=en" target="_blank">🗺️ Download Full Patna Tourist Map</a>
  </div>
  <div class="contact">
    <a href="https://instagram.com/patnafansclub" target="_blank">📩 Message Us on Instagram @patnafansclub</a>
  </div>

  <script>
    // ✨ Sample Data Generator (Replace with your actual data source)
    const placesData = [];
    for(let i=1; i<=1000; i++){
      placesData.push({
        name: `Place #${i}`,
        shortDesc: `Short description for place ${i}`,
        fullDesc: `This is a detailed description about Place #${i}. It has historical, cultural, or scenic value.`,
        img: "https://via.placeholder.com/800x400?text=Place+" + i,
        mapURL: "https://www.google.com/maps/search/?api=1&query=Place+" + i + "+Patna"
      });
    }

    // 🎨 Render cards
    const container = document.getElementById('placesContainer');
    function renderPlaces(list){
      container.innerHTML = '';
      list.forEach(p => {
        const card = document.createElement('div');
        card.className = 'place';
        card.innerHTML = `
          <img src="${p.img}" alt="${p.name}">
          <div class="place-content">
            <h2>${p.name}</h2>
            <p class="short-desc">${p.shortDesc}</p>
            <p>${p.fullDesc}</p>
            <a class="map-button" href="${p.mapURL}" target="_blank">📍 View on Google Maps</a>
          </div>`;
        container.appendChild(card);
      });
    }
    renderPlaces(placesData);

    // 🌐 Live Search
    function searchPlaces(){
      const query = document.getElementById('searchInput').value.toLowerCase();
      const filtered = placesData.filter(p => p.name.toLowerCase().includes(query));
      renderPlaces(filtered);
    }
  </script>

</body>
</html>
