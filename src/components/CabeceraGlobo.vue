<template>
    <div class="header">
        <div class="container">
            <div class="row">
                <div class="col-md-6">
                    <img src="@/assets/img/logo.png" class="logo" alt="">
                </div>       
                    <div class="col-md-6">
                    <input v-model="usuario"  type="text" class="form-control-sm" placeholder="Ingresa tu usuario..." id="txtUsuario">
                </div>                                     
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'CabeceraGlobo',
  data() {
    return{
        usuario:"",
    }
  },
  watch: {
    usuario(nuevoUsuario) {
        if(!this.usuario.trim()==""){
        this.$emit('usuarioEnviado', nuevoUsuario)
        }
        else{
            this.$emit('usuarioEnviado', this.usuario="")
        }

    }
  },
}

</script>

<style scoped>
.header{
    background-color: rgb(59,130, 246);    

}
.logo {
    max-height: 50px;
    margin-top: 25px;
}

#txtUsuario{
    float:right;
    margin: 2rem;
    border-radius: 15px;
    border-color:rgb(59,130, 246);     
    background-color:rgb(208, 226, 241);
    height: 3em;
    width: 15em; 
    padding-left: 15px;    
    margin-left: 3rem;
}
#txtUsuario::placeholder{
    color: blue;    
}

</style>