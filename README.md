<!DOCTYPE html>
<html>
<body>

<button onclick="getLocation()">Duba Wuri</button>
<p id="demo"></p>

<script>
function getLocation() {
  navigator.geolocation.getCurrentPosition(
    function(position) {
      document.getElementById("demo").innerHTML =
      position.coords.latitude + ", " +
      position.coords.longitude;
    },
    function(error) {
      document.getElementById("demo").innerHTML =
      "GPS bai samu ba";
    }
  );
}
</script>

</body>
</html>
