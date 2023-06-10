<template>
    <div class="container mt-5 rounded-3 container-color">
        <div class="row">
            <div class="col-xs-12 col-sm-3 d-flex justify-content-center align-items-center">
                <div class="p-4">
                    <img src="../assets/img/perfil.jpg" alt="imagen perfil" title="Jane Doe"
                        class="rounded-circle border border-3 border-primary imgPerfil">
                </div>
            </div>
            <div class="col-xs-12 col-sm-7 datos">
                <h2><b>Jane Doe</b></h2>
                <p class="datos"><b>Email: </b>jane_doe@gmail.com</p>
                <p class="datos"><b>Fecha de nacimiento: </b>01/05/1996</p>
                <p class="datos"><b>Teléfono: </b>918-936-9585</p>
                <p class="datos"><b>Ciudad: </b>Tokyo, Japón</p>
                <p class="gris">Trabajando en <b>Lawn N</b></p>
            </div>
            <div class="col-xs-12 col-sm-2 " style="position: relative" id="cajaSeguir">
                <button @click="seguirUsuario" :style="{ 'background-color': fondo }" class="btn btn-primary" id="btnSeguir">{{ botonSeguir }}</button>
            </div>
        </div>
    </div>

</template>


<script>

export default {
    name: 'PerfilGlobo',

    data(){
        return{
            botonSeguir: 'Seguir',
            fondo: ''
        }
    },
    methods:{
        seguirUsuario(){
            if(this.botonSeguir== 'Seguir'){
                this.botonSeguir = 'Dejar de Seguir',
                this.fondo =  "blue"
            }
            else
            {
                this.botonSeguir = 'Seguir',
                this.fondo = ''
            }
           
        }
    }
}


</script>



<style scoped>

.container-color{
    background-color: white;

}

.imgPerfil{
    width: 100%;
    object-fit: contain;
    display: block;
    margin: 0.5 auto;
    border: 4px solid #0116f6; padding: 5px; background: #ffff;
}

.datos{
    text-align: left;
    padding-left: 0rem;
}
h2{
    margin-top: 2rem;
}

@media (max-width: 576px) {
    .imgPerfil {
        width: 90%;
        height: 90%;
        object-fit: contain;
        display: block;
        margin: 0 auto;
    }
}

#btnSeguir{    
position: absolute; 
bottom: 40px; 
}

.gris{
color: grey;
}

</style>