<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Discover Patna – Beauty, History & Culture</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Inter', sans-serif;
      background: #f9f9f9;
      color: #333;
    }

    header {
      background: linear-gradient(to right, #0a9396, #005f73);
      color: white;
      text-align: center;
      padding: 60px 20px;
    }
    header h1 {
      font-size: 3em;
      margin-bottom: 10px;
    }
    header p {
      font-size: 1.2em;
      opacity: 0.9;
    }

    .search-bar {
      max-width: 600px;
      margin: 30px auto;
      display: flex;
      align-items: center;
      padding: 8px 16px;
      background: white;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }
    .search-bar input {
      width: 100%;
      border: none;
      font-size: 16px;
      padding: 10px;
      outline: none;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      padding: 20px;
    }

    .place {
      background: white;
      border-radius: 16px;
      margin-bottom: 30px;
      overflow: hidden;
      box-shadow: 0 8px 20px rgba(0,0,0,0.06);
      transition: transform 0.3s ease;
    }
    .place:hover {
      transform: translateY(-5px);
    }
    .place img {
      width: 100%;
      height: auto;
    }
    .place-content {
      padding: 20px;
    }
    .place-content h2 {
      color: #0a9396;
      font-size: 1.6em;
      margin-bottom: 10px;
    }
    .short-desc {
      font-style: italic;
      color: #777;
      margin-bottom: 12px;
    }
    .place-content p {
      line-height: 1.6;
    }

    .map-button {
      display: inline-block;
      margin-top: 15px;
      background: #0a9396;
      color: white;
      padding: 10px 16px;
      text-decoration: none;
      border-radius: 8px;
      transition: background 0.3s;
    }
    .map-button:hover {
      background: #005f73;
    }

    .download-map, .contact {
      text-align: center;
      margin: 50px 0;
    }
    .download-map a, .contact a {
      padding: 14px 24px;
      background: #005f73;
      color: white;
      font-weight: 600;
      border-radius: 10px;
      text-decoration: none;
      font-size: 18px;
      transition: background 0.3s;
    }
    .download-map a:hover, .contact a:hover {
      background: #0a9396;
    }
    .contact a {
      background: #d6336c;
    }
    .contact a:hover {
      background: #ad2858;
    }

    @media (max-width: 768px) {
      header h1 {
        font-size: 2em;
      }
      .place-content h2 {
        font-size: 1.3em;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>🌆 Explore the Beauty of Patna</h1>
    <p>Famous Landmarks, Heritage Spots & Cultural Wonders</p>
  </header>

  <!-- Search Bar -->
  <div class="search-bar">
    <input type="text" id="searchInput" placeholder="🔍 Search for a place..." onkeyup="searchPlaces()">
  </div>

  <!-- Places Container -->
  <div class="container" id="placesContainer">

    <!-- Golghar -->
    <div class="place">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/Golghar%2C_Patna.jpg/800px-Golghar%2C_Patna.jpg" alt="Golghar">
      <div class="place-content">
        <h2>Golghar</h2>
        <p class="short-desc">Iconic granary with panoramic city views</p>
        <p>Built in 1786 by the British, Golghar is a dome-shaped granary with spiral stairs. Climb up to experience breathtaking views of the Ganga river and Patna’s skyline.</p>
        <a class="map-button" href="https://www.google.com/maps/place/Golghar,+Patna/" target="_blank">📍 View on Google Maps</a>
      </div>
    </div>

    <!-- Patna Sahib -->
    <div class="place">
      <img src="https://cdn.sikhnet.com/files/images/2021/11/patna-sahib-1.jpg" alt="Patna Sahib">
      <div class="place-content">
        <h2>Takht Sri Patna Sahib</h2>
        <p class="short-desc">Birthplace of Guru Gobind Singh Ji</p>
        <p>One of the holiest sites in Sikhism, this gurudwara stands on the banks of Ganga. It was built by Maharaja Ranjit Singh and radiates peace, devotion and architectural grace.</p>
        <a class="map-button" href="https://www.google.com/maps/place/Takht+Sri+Harmandir+Sahib,+Patna/" target="_blank">📍 View on Google Maps</a>
      </div>
    </div>

    <!-- Bihar Museum -->
    <div class="place">
      <img src="https://www.holidify.com/images/cmsuploads/compressed/BiharMuseum_20200115134959.jpg" alt="Bihar Museum">
      <div class="place-content">
        <h2>Bihar Museum</h2>
        <p class="short-desc">Modern museum preserving Bihar’s heritage</p>
        <p>A stunning fusion of art, history, and culture. From ancient sculptures to tribal art, the Bihar Museum is a must-visit for anyone curious about Bihar’s glorious past.</p>
        <a class="map-button" href="https://www.google.com/maps/place/Bihar+Museum,+Patna/" target="_blank">📍 View on Google Maps</a>
      </div>
    </div>

    <!-- Gandhi Maidan -->
    <div class="place">
      <img src="https://images.jagran.com/images/2022/jan/Gandhi%20Maidan%20Patna%20(1)1642416304325.jpg" alt="Gandhi Maidan">
      <div class="place-content">
        <h2>Gandhi Maidan</h2>
        <p class="short-desc">Historic public ground with towering Gandhi statue</p>
        <p>Gandhi Maidan has witnessed political revolutions, freedom movement speeches, and public events. Today, it’s a city hub surrounded by malls, markets, and landmarks.</p>
        <a class="map-button" href="https://www.google.com/maps/place/Gandhi+Maidan,+Patna/" target="_blank">📍 View on Google Maps</a>
      </div>
    </div>

    <!-- Agam Kuan -->
    <div class="place">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/Agam_Kuan_Patna.jpg/800px-Agam_Kuan_Patna.jpg" alt="Agam Kuan">
      <div class="place-content">
        <h2>Agam Kuan</h2>
        <p class="short-desc">Ancient Mauryan well with mythical depth</p>
        <p>Known as the "Unfathomable Well", Agam Kuan is associated with Emperor Ashoka. It’s wrapped in mystery, history, and legend – a place both eerie and fascinating.</p>
        <a class="map-button" href="https://www.google.com/maps/place/Agam+Kuan,+Patna/" target="_blank">📍 View on Google Maps</a>
      </div>
    </div>

    <!-- Download Map -->
    <div class="download-map">
      <a href="https://www.google.com/maps/d/u/0/viewer?mid=1XTVrAsaOIhTXaKrqZ3apKqHdZOE&hl=en" target="_blank">🗺️ Download Full Patna Tourist Map</a>
    </div>

    <!-- Instagram Contact Section -->
    <div class="contact">
      <a href="https://instagram.com/patnafansclub" target="_blank">📩 Message Us on Instagram @patnafansclub</a>
    </div>

  </div>

  <!-- JavaScript: Search -->
  <script>
    function searchPlaces() {
      const input = document.getElementById('searchInput').value.toLowerCase();
      const places = document.querySelectorAll('.place');
      places.forEach(place => {
        const title = place.querySelector('h2').textContent.toLowerCase();
        place.style.display = title.includes(input) ? 'block' : 'none';
      });
    }
  </script>

</body>
</html>
