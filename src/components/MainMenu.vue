<template>
    <v-container id="menu-container" class="position-middle m-auto w-fit">
        <v-row v-for="button in buttons" :key="button" no-gutters class="mb-3">
            <button-outline @click="(e : string)=>navigateSomewhere(e)" :text="button" />
        </v-row>
    </v-container>
</template>

<script lang="ts">
import ButtonOutline from '../components/smaller_components/ButtonOutline.vue'
    export default {
        name: 'MainMenu',
        components: {
            ButtonOutline
        },
        data(){
            return{
                buttons: [
                    "Horário de Aulas",
                    "Calendário",
                    "Contatos Importantes",
                    "FAQ",
                    "Admin"
                ]
            }
        },
        methods: {
            navigateSomewhere(value : String){
                this.$router.push('/' + value)
            }
        }
    }
</script>

<style scoped>


.v-container{
    padding: 0;
}

</style>