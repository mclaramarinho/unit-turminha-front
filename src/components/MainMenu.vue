<template>

<v-container fluid id="main-page">
    <div id="main-page-side" class="bg-blue">
        <v-row class="position-middle m-auto">
            <img src="../assets/images/unit-logo.webp" alt="" />
        </v-row>
    </div>

    <div id="main-page-side">
        <v-container no-gutters id="menu-container" class="position-middle m-auto">
            <button-outline margin-bottom text="Horário de Aulas" />
            <button-outline margin-bottom text="Calendário" />
            <button-outline margin-bottom text="Contatos Importantes" />
            <button-outline margin-bottom text="FAQ" />
            <button-outline text="Admin" />
        </v-container>
    </div>
</v-container>

</template>

<script lang="ts">
import ButtonOutline from '../components/smaller_components/ButtonOutline.vue'

    export default {
        name: 'MainMenu',
        components: {
            ButtonOutline
        }
    }
</script>

<style scoped>
#main-page{
    display: flex;
    padding: 0;
    /* height: 100vh; */
    /* width: 100vw; */
    /* position: relative; */
}

#main-page-side{
    position: relative;
    height: 100vh;
    width: 50vw;
}

.v-container{
    padding: 0;
}

#menu-container{
    width: 50%;
}

</style>