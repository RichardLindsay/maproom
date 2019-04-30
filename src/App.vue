<template>
  <div id="app">
    <GoogleMap />
  </div>
</template>

<script>
import GoogleMap from './components/GoogleMap.vue'

export default {
  name: 'app',
  components: {
    GoogleMap
  }
}
</script>

<style>
  html, body, #app {
    width: 100%;
    height: 100%;
    margin: 0;
  }

</style>
