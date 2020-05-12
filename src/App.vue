<template>
  <div id="app">
    <g2></g2>
  </div>
</template>

<script>

  import G2 from './components/G2'

export default {
  name: 'App',
  components: {
    G2
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
