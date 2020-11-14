<template>
  <div class="menu">
    <div class="menu-logo">
      <img class="menu-imglogo" alt="Vue logo" src="./assets/icono-medico.svg">
      Medika.
    </div>

    <ul class="menu-items">
        <router-link class="menu-item" to="/">Home</router-link> 
      <router-link class="menu-item" to="/services">Services</router-link>
      <router-link class="menu-item" to="/usuarios">Usuarios</router-link>
      <router-link class="menu-item" to="/contactanos">Contactanos</router-link>

    </ul>
  </div>

  <router-view/>

  <Footer />
</template>
<script>

    import Footer from './components/Footer.vue'

export default {
    components:{
        Footer
    }
}
</script>

<style lang="scss">
*{
   margin:0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
 

}

.menu {
    background-color: #232c6f;
    width: 100%;
    height: 100px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    &-logo{
      width: 20%;
      height: 100%;
    color: #abb3e8;
    
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
      align-items: center;
    }
    &-imglogo{
      height: 60%;
    }
  &-items{
    width: 40%;
    height: 100%;
      display: flex;
      flex-direction: row;
      justify-content: space-evenly;
      align-items: center;
  }
  &-item{
    list-style: none;
    text-decoration: none;
    color: #abb3e8;
  }
   

}
</style>
