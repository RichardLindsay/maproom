<template>
  <div id="google_map"></div>
</template>

<script>
  export default {
    name: 'GoogleMap',
    data: function() {
      return {
        taprooms: [
          {
            "name": "Wylam Brewery",
            "location": {lat: 54.985925, lng: -1.614847}
          },
          {
            "name": "Wylam Brewery",
            "location": {lat: 53.475139, lng: -2.221963}
          }
        ]
      }
    },
    mounted: function () {
      const map = new google.maps.Map(document.getElementById('google_map'), {
        center: {lat: -34.397, lng: 150.644},
        zoom: 12
      });

      for (var i = 0; i < this.taprooms.length; i++) {
        var marker = new google.maps.Marker({
          position: this.taprooms[i].location,
          map: map,
          title: this.taprooms[i].name
        });
      }

      // navigator.geolocation.getCurrentPosition(function(position) {
      //   var pos = {
      //     lat: position.coords.latitude,
      //     lng: position.coords.longitude
      //   };

      //   map.setCenter(pos)
      // });
    }
  };
</script>

<style scoped>
  #google_map {
    width: 100%;
    height: 100%;
  }
</style>