<template>
  <CabeceraGlobo msg = ""/>
  <PerfilGlobo/>
  <CuerpoGlobo/>
</template>

<script>
import  CabeceraGlobo from './components/CabeceraGlobo.vue'
import CuerpoGlobo from './components/CuerpoGlobo.vue';
import PerfilGlobo from './components/PerfilGlobo.vue';



export default {
  name: 'App',
  components: {
    CabeceraGlobo,
    CuerpoGlobo,
    PerfilGlobo
}
}
</script>

<style>
#app {

  background-color: rgb(244, 244, 245); 
  
  /* font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  */
}
</style>
