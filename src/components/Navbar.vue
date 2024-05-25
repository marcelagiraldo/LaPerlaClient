<script>
import { RouterLink } from 'vue-router'
</script>

<template>
    <nav class="nav">
        <RouterLink class="" :to="{ name: 'principal' }">
            <img alt="Vue logo" class="logo" src="../assets/logo.png" width="125" height="125" />
        </RouterLink>
        <div class="options">
            <RouterLink class="" :to="{ name: 'ingresos' }">Ingresos</RouterLink>
            <RouterLink class="" :to="{ name: 'egresos' }">Egresos</RouterLink>
            <RouterLink class="" :to="{ name: 'nomina' }">Nómina</RouterLink>
            <RouterLink class="" :to="{ name: 'principal' }">Facturas</RouterLink>
            <RouterLink class="" :to="{ name: 'principal' }">Calendario</RouterLink>
        </div>
        <RouterLink class="logout" :to="{ name: 'login' }">
            <svg xmlns="http://www.w3.org/2000/svg" width="60px" height="60px" fill="currentColor" class="bi bi-box-arrow-right" viewBox="0 0 16 16">
                <path fill-rule="evenodd" d="M10 12.5a.5.5 0 0 1-.5.5h-8a.5.5 0 0 1-.5-.5v-9a.5.5 0 0 1 .5-.5h8a.5.5 0 0 1 .5.5v2a.5.5 0 0 0 1 0v-2A1.5 1.5 0 0 0 9.5 2h-8A1.5 1.5 0 0 0 0 3.5v9A1.5 1.5 0 0 0 1.5 14h8a1.5 1.5 0 0 0 1.5-1.5v-2a.5.5 0 0 0-1 0z"/>
                <path fill-rule="evenodd" d="M15.854 8.354a.5.5 0 0 0 0-.708l-3-3a.5.5 0 0 0-.708.708L14.293 7.5H5.5a.5.5 0 0 0 0 1h8.793l-2.147 2.146a.5.5 0 0 0 .708.708z"/>
            </svg>
        </RouterLink>
</nav>
</template>

<style>
.nav{
    background-color: #D1AE53;
    width: 100%;
    display: flex;
    align-items: center;
}
.options{
    margin-left: 200px;
    margin-right: 200px;
    display: flex;
    justify-content: center;
}
.options a{
    margin-left: 70px;
    color: black;
    text-decoration: none;
}
.logout svg{
    color: black;
}
</style>
