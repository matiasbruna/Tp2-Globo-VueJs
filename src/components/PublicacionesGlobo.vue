<template>
    <div class="container mt-4 container-color rounded-3 ">
        <div class="container">
            <h5 class="gris">Publicado hace 1 semana</h5>
        </div>
        <img src="../assets/img/img1.jpg" alt="" class="imgPublicacion rounded-3">
        <div class="container">
            <button class="btn btn-primary" id="btnMeGusta">Me Gusta</button>
            <p id="txtLike"><b>200 Likes</b></p>
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
        </div>

        <div class="container mt-5 mb-0 p-0">
            <input class="form-control-sm comment mb-0" type="text" id="txtComentarios"
                placeholder="Deja tu comentario...">
            <button class="btn btn-primary" id="btnComentar">Comentar</button>
        </div>
        <div class="container ml-4" id="divAlerta"></div>
        <br>
    </div>

</template>

<script>
export default{
    name: 'PulicacionesGlobo'
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