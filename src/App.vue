<template>
  <CabeceraGlobo msg = ""/>
  <CuerpoGlobo/>
</template>

<script>
import  CabeceraGlobo from './components/CabeceraGlobo.vue'
import CuerpoGlobo from './components/CuerpoGlobo.vue';



export default {
  name: 'App',
  components: {
    CabeceraGlobo,
    CuerpoGlobo
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
