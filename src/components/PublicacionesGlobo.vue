<template>
    <div class="container mt-4 container-color rounded-3 ">
        <div class="container">
            <h5 class="gris">Publicado hace 1 semana</h5>
        </div>
        <img src="../assets/img/img1.jpg" alt="" class="imgPublicacion rounded-3">
        <div class="container">
            <button @click="DarLike" :style="{'background-color': fondo }" class="btn btn-primary" id="btnMeGusta">{{ botonMeGusta }}</button>
            <p id="txtLike"><b>{{like}} Likes</b></p>
        </div>
        <br>
        <h5 class="gris">Comentarios</h5>
        <br>

        <div class="container">
            <p class="comment"><strong>Juan Perez </strong> ¡Wow, esa foto de Tokio es impresionante!
                (っ-●益●)っ ,︵‿ </p>
        </div>

        <div class="container">
            <p class="comment"><strong>Kathleen J Rennie </strong> ¡Esta foto de Tokyo es simplemente
                espectacular! Me trae tantos recuerdos.</p>
        </div>
        <div class="container" id="divComentarios"> 
            <p class="comment" v-for = "(arrayComentario, index) in arrayComentarios" :key="index">
               {{ arrayComentario.usuario}} : {{ arrayComentario.comentario }}
             
               <button class="btn-eliminarCometario" @click="EliminarComentarios(index)">Eliminar</button>
            </p>              
        </div>
        <form @submit.prevent="AgregarComentarios">           

            <div class="container mt-5 mb-0 p-0">
                <input v-model="comentario" class="form-control-sm comment mb-0" type="text" id="txtComentarios"
                    placeholder="Deja tu comentario...">
                <button type="submit" class="btn btn-primary" id="btnComentar">Comentar</button>
            </div>
            
            <div class="container ml-4" id="divAlerta">
                <p :style="{'color': ColorErrores }">{{ errores }}</p>
            </div>
            <br>
        </form>   

        
    </div>
         
</template>

<script>
//import { string } from 'yargs'



export default{
    name: 'PublicacionesGlobo',
    props:{
        //usuario:String
    },
    data()
    {
        return{
          botonMeGusta:"Me gusta",
          fondo:"",
          like:200,
          comentario:"",
          arrayComentarios:[],
          errores:"",
          ColorErrores:"red",
          
          
        }
    },
    methods:
    {
        DarLike(){
           
            if(this.botonMeGusta=="Me gusta"){
                this.botonMeGusta="No me gusta"
                this.fondo="blue"
                this.like++
            }
            else{

                this.botonMeGusta="Me gusta"
                this.fondo=""
                this.like--
            }
        },
        AgregarComentarios(){
            
            if(!this.comentario.trim()=="")
            {
                
                this.errores=""
                this.arrayComentarios.push({
                usuario:this.valorProps,
                comentario: this.comentario                
                })
                this.comentario=""
            }
            else{
                this.errores="Debe ingresar un comentario!!"                
            }           
        },
        EliminarComentarios(Index){

            this.arrayComentarios.splice(Index, 1);
        }

    }
}
</script>

<style scoped>

.container-color{
    background-color: white;

}
h5{ 
    position: relative;
    bottom: -1rem;
    margin-left: 1rem;
}

.imgPublicacion{
width: 90%;
margin:2rem;
margin:1rem;
}
.gris{
color: grey;
}

.col-sm{
float: right;
margin-top: 13rem;
padding-left: 8rem;
padding-top: 15px;


}
#txtLike{
    float: right;
}
.btn-outline-primary{
    color:white;
    background-color: rgb(59,130, 246);
}
.abs-center {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }
.btn-eliminarCometario
{
    color: red;
    background-color:rgb(228, 222, 222);
    border: beige;
    border-radius: 7px;
}
.form-control-sm.comment
{
    width: 400px;
    margin-bottom: 40px;
    margin-left: 20px;    
}

</style>