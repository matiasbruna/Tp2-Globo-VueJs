<template>
<div class="header">
    <div class="container">
            <div class="row">
                <div class="col-6 col-sm-6">
                    <img src="@/assets/img/logo.png" class="logo" alt="">
                </div>
                <div class="col-6 col-sm-6">
                    {{ msg }}
                </div>

                <div class="col-6 col-sm-6">
                    <input type="text" class="form-control-sm" placeholder="Ingresa tu usuario..." id="txtUsuario">
                </div>
            </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'CabeceraGlobo',
  props: {
    msg: String
  }
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

</style>