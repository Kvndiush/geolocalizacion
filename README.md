geolocalizacion.html 
<!DOCTYPE html>
<html>
<head>
  <title>Geolocalización</title>
  <script>
    function getLocation() {
      if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition);
      } else {
        document.getElementById("location").innerHTML = "Geolocalización no soportada por este navegador.";
      }
    }

    function showPosition(position) {
      document.getElementById("location").innerHTML = 
      "Latitud: " + position.coords.latitude + "<br>" + 
      "Longitud: " + position.coords.longitude;
    }
  </script>
</head>
<body onload="getLocation()">
  <h1>Tu ubicación actual</h1>
  <p id="location">Obteniendo ubicación...</p>
</body>
</html>
 
