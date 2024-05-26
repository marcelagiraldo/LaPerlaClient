<script>
import Navbar from './Navbar.vue'
import axios from 'axios';
export default {
    components: {
        Navbar
    },
    data() {
        return {
            payrolls: [],
        };
    },
    mounted() {
        this.getPayroll();
    },
    methods:{
        async getPayroll() {
            try {
                const response = await axios.get('http://localhost:8001/payroll/payrolls');
                this.payrolls = response.data
                console.log(this.payrolls);
                console.log("Id",this.payrolls.length + 1);
            } catch (error) {
                console.error('Error al obtener Nómina:', error);
            }
        },
        async create_payroll() {
            try {
                const newIncome = {
                    'id': this.payrolls.length + 1,
                    'date_':this.datePayroll,
                    'activity':this.activityPayroll,
                    'category':this.categorySelect,
                    'responsible':this.resposiblePayroll,
                    'observation':this.observationPayroll
                }
                const response = await axios.post(`http://localhost:8001/payroll/payrolls/`,newIncome);
                this.payrolls.push(response.data);
                this.getPayroll()
                this.$router.push({ name: 'nomina' });
                window.location.reload();
            } catch (error) {
                console.error('Error al crear Nomina:', error);
            }
        }
    }
}
</script>

<template>
    <Navbar/>
    <div class="content">
        <h1>Agregar.</h1>
        <form class="form-group">
            <div class="content-left">
                <div class="fecha">
                    <label for="formGroupExampleInput" class="form-label">Fecha *</label>
                    <input type="date" class="form-control" id="formGroupExampleInput" placeholder="Usuario" v-model="datePayroll">
                </div>
                <div class="categoria">
                    <label for="formGroupExampleInput" class="form-label">Categoría *</label>
                    <select class="form-select" id="inputGroupSelect01" v-model="categorySelect">
                        <option selected>Choose...</option>
                        <option value="Café">Café</option>
                        <option value="Platano">Platano</option>
                    </select>
                </div>
                <div class="actividad">
                    <label for="formGroupExampleInput" class="form-label">Actividad *</label>
                    <input type="text" class="form-control" id="formGroupExampleInput" placeholder="Usuario" v-model="activityPayroll">
                </div>
                <div class="responsable">
                    <label for="formGroupExampleInput" class="form-label">Repsonsable *</label>
                    <input type="text" class="form-control" id="formGroupExampleInput" placeholder="Usuario" v-model="resposiblePayroll">
                </div>
            </div>
            <div class="content-right">
                <div class="mb-3">
                    <label for="exampleFormControlTextarea1" class="form-label">Observación</label>
                    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3" v-model="observationPayroll"></textarea>
                </div>
            </div>
            <RouterLink class="entrar" :to="{ name: 'nomina' }">
                <button type="submit" class="submit-btn" @click="create_payroll"><svg xmlns="http://www.w3.org/2000/svg" width="60px" height="60px" fill="currentColor" class="bi bi-check" viewBox="0 0 16 16">
                    <path d="M10.97 4.97a.75.75 0 0 1 1.07 1.05l-3.99 4.99a.75.75 0 0 1-1.08.02L4.324 8.384a.75.75 0 1 1 1.06-1.06l2.094 2.093 3.473-4.425z"/>
                </svg></button>
            </RouterLink>
        </form>
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
