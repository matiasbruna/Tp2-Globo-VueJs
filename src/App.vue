<template>
  <CabeceraGlobo msg = ""/>

  <PerfilGlobo/>

  <div class="container mt-4 p-0">
    <div class="row">
        <div class="col-7">

            <PublicacionesGlobo/>

        </div>
        <div class="col-5">

          <SobreMiGlobo/>  
                 
        </div>
    </div>
  </div>
  
</template>

<script>
import  CabeceraGlobo from './components/CabeceraGlobo.vue'
import PerfilGlobo from './components/PerfilGlobo.vue';
import PublicacionesGlobo from './components/PublicacionesGlobo.vue';
import SobreMiGlobo from './components/SobreMiGlobo.vue';


export default {
  name: 'App',
  components: {
    CabeceraGlobo,
    PerfilGlobo,
    SobreMiGlobo,
    PublicacionesGlobo
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
