<script setup>
import ButtonsComponent from './components/ButtonsComponent.vue';
import EventGlobal from './components/EventGlobal.vue';
import EventStyle from './components/EventStyle.vue';
import EventPopUp from './components/EventPopUp.vue';


</script>


<template>

  <header>
    <h1>Eventos</h1>
  </header>



    <!-- <ButtonsComponent /> -->
    <!-- <EventGlobal /> -->
    <!-- <EventStyle /> -->
     <EventPopUp />




</template>


<style scoped>
header{
    background-color: #d19627;
    padding: 20px;
    text-align: center;
    border-bottom: 8px solid #6c4e15;
}
h1{
    color: white;
}

</style>