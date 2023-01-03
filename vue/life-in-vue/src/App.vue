<template>
  <div id="app">
    <QuadradosLife/>
  </div>
</template>

<script>
import QuadradosLife from './components/Quadrados.vue'

export default {
  name: 'App',
  components: {
    QuadradosLife
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;

}
</style>
