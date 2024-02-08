<template>
    <v-container fluid id="main-page">
        <NavBar />
        <div id="main-page-side" class="bg-blue show-lg">
            <v-row class="position-middle m-auto">
                <img src="../assets/images/unit-logo.webp" alt="" />
            </v-row>
        </div>

        <div id="main-page-side" class="mx-sm-auto ">
            <MainMenu v-if="currentDisplay===1" />
            <ClassSchedule v-if="currentDisplay===2" />
        </div>
    </v-container>
</template>

<script lang="ts">
import NavBar from '../components/smaller_components/NavBar.vue'
import MainMenu from '../components/MainMenu.vue'
import ClassSchedule from '../components/ClassSchedule.vue'

export default {
    name: 'PublicView',
    components: {
        NavBar, MainMenu, ClassSchedule
    },
    data(){
        return{
            currentDisplay: 0,
        }
    },
    watch:{
        $route(to, from){
            this.checkPath()
            console.log(this.currentDisplay);
            
        },
    },
    created(){
        this.checkPath()
        console.log(this.currentDisplay);

    },
    methods: {
        checkPath(){
            switch (this.$route.path) {
                    case ('/' || ''):
                        this.currentDisplay = 1
                        break;
                    case ('/calendario'):
                        this.currentDisplay = 2
                        break;
                    case ('/horario-de-aulas'):
                        this.currentDisplay = 3
                        break;
                    case ('/contatos-importantes'):
                        this.currentDisplay = 4
                        break;
                    case ('/faq'):
                        this.currentDisplay = 5
                        break
                }
        }
    }
}
</script>


<style scoped>
#main-page{
    display: flex;
    padding: 0;
}

#main-page-side{
    position: relative;
    height: 100vh;
    width: 50vw;
}
@media (max-width:768px) {
    #main-page-side{
        width: 80vw !important;
    }
}
</style>