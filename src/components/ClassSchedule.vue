<template>
    <v-container class="position-middle calendar-container m-auto">
      <v-row no-gutters class="">
        <v-col></v-col>
        <v-col v-for="weekday in weekdays" :key="weekday" class="weekday_item">
          <p class="weekday_content">{{ weekday }}</p>
        </v-col>
      </v-row>
    </v-container>
</template>

<script lang="ts">
    export default {
        name: 'ClassSchedule',
        data(){
          return{
            weekdays: ['Seg', 'Ter', 'Qua', 'Qui', 'Sex'],
          }
        }, 
        methods: {
        }
    }
</script>

<style scoped>

.weekday_item{
  border-color: var(--dark-blue) !important;
  border-style: solid !important;
  border-width: thin !important;
}
.weekday_content{
  font-size: 1.2rem !important;
  text-align: center;
}

.calendar-container{
  min-width: 80%;
  max-width: 95%;
}
.v-container{
  padding: 0 !important;
}
</style>