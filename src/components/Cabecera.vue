<template>
    <div class="text-center">
        <img alt="Vue logo" src="@/assets/logo.png">
        <h1>{{tituloApp}}</h1>
    </div>
</template>

<script>
export default {
    name: 'Cabecera',
    props:{
        tituloApp: String
    }
}
</script>

<style scoped>

</style>