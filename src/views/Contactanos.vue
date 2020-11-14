<template>
 <div class="contenedor">
    <div class="mapa">
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3901.1454378603025!2d-77.01354748561712!3d-12.102194346228107!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9105c875e1022387%3A0x7b7c14e1d0fc1b4f!2sClinica%20Veterinaria%20Groomers%20Sede%20San%20Borja%20-%20San%20Isidro!5e0!3m2!1ses-419!2spe!4v1596902440420!5m2!1ses-419!2spe" width="600" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>

    </div>
    <div class="info">
            <Informacion />

    </div>


    <div class="formulario"> <Formulario /> </div>
    <div class="unete"> Uniete a nuestra red de contactos <span>!!!</span></div>

  
  </div>
</template>

<script>
    import Formulario from '../components/Formulario.vue'
    import Informacion from '../components/Informacion.vue'

export default {
    components:{
        Formulario,
        Informacion
    }
}
</script>

<style lang="scss" scoped>
.mapa{
    width: 50%;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    iframe{
    height: 80%;        
        object-fit: contain;
        
    }
}
.info{
    width: 50%;
    height: 400px;
}

.unete{
    width: 50%;
    height: 400px;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 5%;
    color: #d8d8d8;
    line-height: 70px;
    & span{
        color: #d2b694;
        font-size: 65px;
    }
}
.formulario{
    width: 50%;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.contenedor{
    background-color: #222222;
    display: flex;
    flex-wrap: wrap;
}
</style>