<template>
    <div class="col-12 text-center">
        <img alt="Vue logo" src="@/assets/logo-cinema.png" class="mb-5">
        <h1 v-text="tituloApp"></h1>
        <div v-html="integrantesHtml" class="mb-5"></div>
    </div>
</template>

<script>
export default {
    name: 'Cabecera',
    props:{
        tituloApp: String,
        integrantes: Array
    },
    data() {
        return {
            
        }
    },
    computed: {
        integrantesHtml(){
            return /*html*/ `
                <h2><i>${this.integrantes.join(' - ')}</i></h2>
            `
        }
    },
}
</script>

<style scoped>

</style>