<template>
  <div id="app" class="container">
    <div class="row">
      <Cabecera tituloApp="Esta es mi aplicacion" :integrantes="['Mi nombre aquí', 'Otro nombre aquí']" />
      <ListaPelicula />
    </div>
  </div>
</template>

<script>
import Cabecera from './components/Cabecera.vue'
import ListaPelicula from './components/ListaPelicula.vue'

export default {
  name: 'App',
  components: {
    Cabecera,
    ListaPelicula
  },
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
