<template>
  <div id="app">
    <PetriNetMain />
  </div>
</template>

<script>
import PetriNetMain from './components/PetriNetMain.vue'

export default {
  name: 'app',
  components: {
    PetriNetMain
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  text-align: center;

}
</style>
