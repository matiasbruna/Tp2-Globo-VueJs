<template>
  <div class="container">
    <CabeceraGlobo  @usuarioEnviado="recibirUsuario"/>
  </div>
   
  <div class="container">
    <PerfilGlobo/>
  </div>
  
  <div class="container">
    <div class="container mt-4 ">
      <div class="row">
          <div class="col-md-7">
              <PublicacionesGlobo :usuario ="usuario"/>
          </div>
          <div class="col-md-5">
            <SobreMiGlobo/>          
          </div>
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
  data(){
    return{
      usuario: ''
    }
  },
  components: {
    CabeceraGlobo,
    PerfilGlobo,
    SobreMiGlobo,
    PublicacionesGlobo
},
methods:{
  recibirUsuario(valor){
    this.usuario = valor
  }
}
}
</script>

<style>
#app {

  background-color: rgb(244, 244, 245); 
  font-family: 'Montserrat', sans-serif;
  
}
</style>
