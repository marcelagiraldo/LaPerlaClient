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
        <label for="">FECHA</label>
        <h1>Balance actual:</h1>
        <label for="">$</label>
        <div id="carouselExampleFade" class="carousel slide carousel-fade">
            <div class="carousel-inner">
                <div class="carousel-item ">
                <img src="https://www.semana.com/resizer/jimRCfZU3kcVz7eYsHdN6vpLEkE=/1280x720/smart/filters:format(jpg):quality(80)/cloudfront-us-east-1.images.arcpublishing.com/semana/MGSRCROCY5GETHHQC2XBMM2CEQ.jpg" class="d-block w-200" alt="...">
                </div>
                <div class="carousel-item active">
                <img src="https://mundocafeto.com/wp-content/uploads/2020/02/planta-de-cafe-caracteristicas-750x440.jpg" class="d-block w-200" alt="...">
                </div>
                <div class="carousel-item">
                <img src="https://i0.wp.com/farallonesdelcitara.bioexploradores.com/wp-content/uploads/2022/10/IMG_3619-2.jpg?resize=790%2C415&ssl=1" class="d-block w-200" alt="...">
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div>
    </div>

</template>

<style>
.content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
}
.carousel-inner {
    width: 900px; /* Establecer el ancho deseado */
    overflow: hidden; /* Evitar desbordamiento de imágenes más grandes */
}

.carousel-item img {
    max-width: 100%;
    height: auto;
    overflow: hidden;
}
</style>
