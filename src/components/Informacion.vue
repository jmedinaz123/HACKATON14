<template>
  <div class="informacion">
      <div class="datoEmpresa">
          <div class="datoEmpresa-imagen">
              <img src="../assets/ContactanosImg1.jpg" alt="">
          </div>
          <div class="datoEmpresa-info">
              <h2>Dirección:</h2>
              <h3>San Isidro </h3>
          </div>
      </div>

        <div class="datoEmpresa">
          <div class="datoEmpresa-imagen">
              <img src="../assets/ContactanosImg2.png" alt="">
          </div>
          <div class="datoEmpresa-info">
              <h2>Telf:</h2>
              <h3>(01)333-4444 +999 999 999,</h3>
          </div>
      </div>
            <div class="datoEmpresa">
          <div class="datoEmpresa-imagen">
              <img src="../assets/ContactanosImg3.png" alt="">
          </div>
          <div class="datoEmpresa-info">
              <h2>Horario de Atención:</h2>
              <h3>Lun. – Sáb.: 9 am a 7:30 pm,</h3>
          </div>
      </div>
            <div class="datoEmpresa">
          <div class="datoEmpresa-imagen">
              <img src="../assets/ContactanosImg4.jpg" alt="">
          </div>
          <div class="datoEmpresa-info">
              <h2>Correo Electrónico:</h2>
              <h3>info@clinicaveterinariaejea.com</h3>
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.informacion{
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    padding: 5%;
   
}
.datoEmpresa{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 100%;
    height: 15%;

    &-imagen{
        width: 30%;
        height: 100%;
        display: flex;
        justify-content: center;
        img{
            height: 100%;
            border-radius: 80%;
        }
    }
    &-info{
        width: 60%;
        height: 100%;
        h2{
            font-size: 150%;

            color:#bb915e;

        }
        h3{
            font-size: 100%;
            margin-left: 20%;
            color: #8a8576;
        }
    }
}
</style>