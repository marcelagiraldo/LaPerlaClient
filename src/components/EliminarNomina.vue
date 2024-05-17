<script>
import Navbar from './Navbar.vue'
export default {
  components: {
    Navbar
  },
}
</script>

<template>
    <Navbar/>
    <div class="content">
        <h1>Eliminar</h1>

        <table>
            <tr>
                <th>Fecha</th>
                <th>Actividad</th>
                <th>Responsable</th>
                <th>Observación</th>
                <th><input class="form-check-input" type="checkbox" value="" id="flexCheckDefault"></th>
            </tr>
            <tr>
                <td>Fecha</td>
                <td>Actividad</td>
                <td>Responsable</td>
                <td>Observación</td>
                <td><input class="form-check-input" type="checkbox" value="" id="flexCheckDefault"></td>
            </tr>
            <tr>
                <td>Fecha</td>
                <td>Actividad</td>
                <td>Responsable</td>
                <td>Observación</td>
                <td><input class="form-check-input" type="checkbox" value="" id="flexCheckDefault"></td>
            </tr>
            <tr>
                <td>Fecha</td>
                <td>Actividad</td>
                <td>Responsable</td>
                <td>Observación</td>
                <td><input class="form-check-input" type="checkbox" value="" id="flexCheckDefault"></td>
            </tr>
            <tr>
                <td>Fecha</td>
                <td>Actividad</td>
                <td>Responsable</td>
                <td>Observación</td>
                <td><input class="form-check-input" type="checkbox" value="" id="flexCheckDefault"></td>
            </tr>
        </table>
        <RouterLink class="entrar" :to="{ name: 'nomina' }">
            <svg xmlns="http://www.w3.org/2000/svg" width="60px" height="60px" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425z"/>
            </svg>
        </RouterLink>
    </div>

</template>

<style>
.content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.container{
    display: flex;
    justify-content: center;
}
.content-left{
    width: 80%;
    margin: 20px;
}
.content-right{
    width: 80%;
    margin: 20px;
}
.valor{
    display: flex;
}
.entrar{
    display: flex;
    justify-content: center;
    align-items: center;
    color: black;
    width: 10%;
    height: 40px;
    font-size: 30px;
    margin: 90px;
    background-color: #CF9339;
    border-style: none;
    text-decoration: none;
}
table{
    margin: 90px;
    border-collapse: collapse;
    border: 2px solid rgb(182, 178, 178); /* Borde de la tabla */
    width: 60%;
    tr:nth-child(even) {background-color: #D9D9D9;}
}
th {
  background-color: #CF9339;
  color: white;
}
</style>
