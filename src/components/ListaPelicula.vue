<template>
    <div class="col-12 col-sm-6 col-md-4 mx-auto">
        <!-- Es una lista con BootstrapVue pero el mapeo al documento final son solo divs (no semánticos) -->
        <b-list-group>
            <b-list-group-item v-for="pelicula of peliculas" v-bind:key="pelicula.id" 
            class="d-flex justify-content-between align-items-center">
                {{pelicula.nombre}}
                <b-badge :variant="pelicula.anio >= 2000 ? 'primary' : 'warning' " pill>Año: {{pelicula.anio}}</b-badge>
            </b-list-group-item>
        </b-list-group>
    </div>
</template>

<script>
export default {
    name:'ListaPelicula',
    data() {
        return {
            peliculas: [
                {nombre:"Pelicula número 1.", anio:1988},
                {nombre:"Pelicula número 2.", anio:2005},
                {nombre:"Pelicula número 3.", anio:2006},
                {nombre:"Pelicula número 4.", anio:2003},
                {nombre:"Pelicula número 5.", anio:1995},
            ]
        }
    },
}
</script>

<style scoped>

</style>