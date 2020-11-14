<template>
  <footer class="footer">


      <section class="footer-secction secction-info">
                    <Informacion />

      </section>


      <section class="footer-secction secction-Logo">
        <img src="../assets/icono-medico.svg" alt="">
        <h1>Medika</h1>
      </section>


      <section class="footer-secction secction-Redes">
          <h1>Síguenos en Nuestras Redes Sociales</h1>
          <div class="secction-Redes-iconos" >
              <img src="../assets/RS1.png" alt="">
              <img src="../assets/RS2.jpg" alt="">
              <img src="../assets/RS3.png" alt="">

          </div>
      </section>

  </footer>
</template>

<script>
    import Informacion from './Informacion.vue'

export default {
  components:{
        Informacion
    }
    }
</script>

<style lang="scss" scoped>
.footer{
  width: 100%;
  height: 300px;
  background-color: #232323;
  display: flex;
  flex-direction: row;
    &-secction{
      width: 33%;
      height: 100%;
    }
}
.secction{
  &-Logo{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: #abb3e8;
    font-size: 20px;
    img{
      height:  50%;
    }
  }
  &-Redes{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 5%;
    h1{
      color:#bb915e;
      font-size: 15px;
    }
    &-iconos{
      width: 100%;
      height: 30%;
      margin-top: 10px;
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
    }
    img{
      height: 70%;
		  object-fit: contain;
      border-radius: 100%;
    }
  }

}
</style>