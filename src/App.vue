<template>
  <div id="app">
    <nav-bar></nav-bar>
    <get-quote></get-quote>
  </div>
</template>

<script>
import GetQuote from './components/GetQuote.vue'
import NavBar from './components/NavBar.vue'

export default {
  name: 'app',
  components: {
    GetQuote,
    NavBar
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
