<template>
  <div id="app">
    <Lista/>
    <Card/>
  </div>
</template>

<script>
import Lista from './components/ListaEmpleos.vue'
import Card from './components/CardEmpleo.vue'

export default {
  name: 'App',
  components: {
   Lista,
   Card
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
