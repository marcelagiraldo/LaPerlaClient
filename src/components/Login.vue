<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
    <div class="content">
        <img alt="Vue logo" class="logo" src="../assets/logo.png" width="125" height="125" />
        <h1>INICIO DE SESIÓN</h1>
        <div class="usuario">
            <label for="formGroupExampleInput" class="form-label">Usuario</label>
            <input type="text" class="form-control" id="formGroupExampleInput" placeholder="Usuario">
        </div>
        <div class="contrasena">
            <label for="formGroupExampleInput2" class="form-label">Contraseña</label>
            <input type="password" class="form-control" id="formGroupExampleInput2" placeholder="Contraseña">
        </div>
        <!-- <a href="" class="entrar">Entrar</a> -->
        <RouterLink class="entrar" :to="{ name: 'principal' }">Entrar</RouterLink>

    </div>
</template>

<style scoped>
body{
    width: 100%;
    height: 100%;
}
.content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
}
.usuario{
    display: flex;
    flex-direction: column;
    margin: 30px;
}
.usuario input{
    width: 700px;
    height: 40px;
    font-size: 30px;
    background-color: #D9D9D9;
    border-style: none;
}
.contrasena{
    display: flex;
    flex-direction: column;
    margin: 30px;
}
.contrasena input{
    width: 700px;
    height: 40px;
    font-size: 30px;
    background-color: #D9D9D9;
    border-style: none;
}
.entrar{
    display: flex;
    justify-content: center;
    align-items: center;
    color: black;
    width: 30%;
    height: 40px;
    font-size: 30px;
    margin: 90px;
    background-color: #CF9339;
    border-style: none;
    text-decoration: none;
}
</style>
