<template>
  <CabeceraGlobo msg = "Hola Papa"/>
  <CuerpoGlobo/>
  <h1>Javi ....</h1>

  
  
 
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import  CabeceraGlobo from './components/CabeceraGlobo.vue'
import CuerpoGlobo from './components/CuerpoGlobo.vue';



export default {
  name: 'App',
  components: {
    HelloWorld,
    CabeceraGlobo,
    CuerpoGlobo
}
}
</script>

<style>
#app {
  
  /* font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  */
}
</style>
