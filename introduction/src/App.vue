<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Lista_tareas></Lista_tareas>
</template>

<script>
import Lista_tareas from './components/Lista_tareas.vue'

export default {
  name: 'App',
  components: {
    Lista_tareas
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
