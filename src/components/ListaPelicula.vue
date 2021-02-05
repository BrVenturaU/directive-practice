<template>
    <div class="col-12 col-sm-6 col-md-4 mx-auto">
        <!-- Es una lista con BootstrapVue pero el mapeo al documento final son solo divs (no semánticos) -->
        <b-list-group>
            <b-list-group-item class="mx-auto d-flex justify-content-between align-items-center" active>
                <h3 v-format="'uppercase'">Lista de peliculas</h3>
            </b-list-group-item>
            <b-list-group-item v-for="(pelicula, indice) of peliculas" v-bind:key="pelicula.id" 
                @click="aumentarVistas(indice)"
                class="puntero d-flex justify-content-between align-items-center">
                <strong>{{pelicula.nombre}} ({{pelicula.anio}})</strong>
                <b-badge :variant="pelicula.vistas >= 10 && pelicula.vistas < 20 ? 'primary' : pelicula.vistas >= 20 ? 'success' : 'warning' " pill>Vistas: {{pelicula.vistas}}</b-badge>
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
                {nombre:"Pelicula número 1.", anio:1988, vistas:10},
                {nombre:"Pelicula número 2.", anio:2005, vistas:0},
                {nombre:"Pelicula número 3.", anio:2006, vistas:8},
                {nombre:"Pelicula número 4.", anio:2003, vistas:1},
                {nombre:"Pelicula número 5.", anio:1995, vistas:3},
            ]
        }
    },
    methods:{
        aumentarVistas(indice){
            this.peliculas[indice].vistas++;
        }
    }
}
</script>

<style scoped>
    .puntero{
        cursor: pointer;
    }
    .puntero:hover{
        color: #007bff;
    }
</style>