<template>
  <div id="app">
    <CardInfo />
  </div>
</template>

<script>
import CardInfo from './components/CardInfo'

export default {
  name: 'App',
  components: {
    CardInfo
  }
}
</script>

<style>
body{
  background: lavender;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
