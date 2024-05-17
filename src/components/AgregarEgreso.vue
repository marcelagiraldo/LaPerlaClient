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
        <h1>Agregar.</h1>
        <div class="container">
            <div class="content-left">
                <div class="fecha">
                    <label for="formGroupExampleInput" class="form-label">Fecha *</label>
                    <input type="date" class="form-control" id="formGroupExampleInput" placeholder="Usuario">
                </div>
                <div class="categoria">
                    <label for="formGroupExampleInput" class="form-label">Categoría *</label>
                    <select class="form-select" id="inputGroupSelect01">
                        <option selected>Choose...</option>
                        <option value="1">One</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <label for="formGroupExampleInput" class="form-label">Valor *</label>
                <div class="valor">
                    <span class="input-group-text">$</span>
                    <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
                    <span class="input-group-text">.00</span>
                </div>
            </div>
            <div class="content-right">
                <div class="mb-3">
                    <label for="exampleFormControlTextarea1" class="form-label">Descripción</label>
                    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                </div>
                <div class="mb-3">
                    <label for="exampleFormControlTextarea1" class="form-label">Observación</label>
                    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
                </div>
            </div>
        </div>
        <RouterLink class="entrar" :to="{ name: 'egresos' }">
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
</style>
