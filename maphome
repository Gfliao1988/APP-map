<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Our Locations</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />

  <style>
    html, body, #map {
      height: 100%;
      margin: 0;
    }
  </style>
</head>
<body>

<div id="map"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
  // Map setup
  var map = L.map('map', {
    scrollWheelZoom: false,
    dragging: true,
    zoomControl: true
  }).setView([53.3498, -6.2603], 13); // Default center (Dublin)

  // Tile layer (OpenStreetMap)
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '© OpenStreetMap contributors'
  }).addTo(map);

  // Your locations
  const locations = [
    { name: "Dublin HQ", lat: 53.3498, lng: -6.2603 },
    { name: "Pickup Point A", lat: 53.3438, lng: -6.2546 },
    { name: "Dropoff Spot B", lat: 53.3554, lng: -6.2711 }
  ];

  // Add markers
  locations.forEach(loc => {
    L.marker([loc.lat, loc.lng])
      .addTo(map)
      .bindPopup(loc.name);
  });

  // Optional: Fit map to show all markers
  const bounds = L.latLngBounds(locations.map(l => [l.lat, l.lng]));
  map.fitBounds(bounds, { padding: [30, 30] });

</script>
</body>
</html>
