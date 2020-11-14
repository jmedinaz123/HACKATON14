<template>
  <h1>{{nombre}}</h1>
    <div class="ContenedorCard">
        <div class="card" v-for="user in usuarios" v-bind:key="user.id">
            
            <div class="card-foto">
            <img class="card-img" alt="foto Predeterminado" src="../assets/icono-contacto.svg">

            </div>

            <div class="card-info info">
                <div class="info-titulo">
                    {{user.username}}
                </div>
                <div class="descripcion">
                    <div class="info-descripcion">
                        <div class="info-llave">Nombre:</div>   <div class="info-valor">{{user.name}}</div>
                    </div>
                    <div class="info-descripcion">
                        <div class="info-llave">Correo:</div>   <div class="info-valor">{{user.email}}</div>
                    </div>
                    <div class="info-descripcion">
                        <div class="info-llave">Telefono:</div>   <div class="info-valor">{{user.phone}}</div>
                    </div>
                    <div class="info-descripcion">
                        <div class="info-llave">Compañia:</div>   <div class="info-valor">{{user.company.name}}</div>
                    </div>
                </div>
            </div>
                

        </div>
    </div>
</template>

<script>
export default {
name:"Usuarios",
data(){
    return{
        nombre:"USUARIOS",
        usuarios:[]
    }
},


methods:{
    async getUsuarios(){
        const info=await fetch('https://jsonplaceholder.typicode.com/users')
        const data =await info.json();
        this.usuarios=data
    }
},

created(){
    this.getUsuarios();
}


}
</script>

<style lang="scss" scoped>
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
h1{
    font-size: 50px;
    text-align: center;
    color: #bb915e;
}
.ContenedorCard{
    min-height: 100vh;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    background-color: #222222;
    

}
.card{
    width: 350px;
    height: 150px;
    margin: 20px;
    border: 1px solid black;
    display: flex;
    flex-direction: row;
    background-color: #d1d1d1;
    color: #d1d1d1;
    &-foto{
        width: 35%;
        display: flex;
        justify-content: center;
        align-items: center;

    }
    &-img{
        width: 80%;
        background-color: white;


    }
}
.info{
        width: 65%;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 5px;
        &-titulo{
            width: 100%;
            height: 20%;
            margin-bottom: 10px;
            background-color: #d2b694;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 20px;
        }
        &-descripcion{
            width: 100%;

            display: flex;
            flex-direction: row;
            margin:2.5px 0 2.5px 0;

        }
        &-llave{
            width: 35%;
            font-size: 14px;
            text-decoration: underline;
             display: flex;
            flex-direction: row;
            justify-content: flex-start;
            align-items: center;
            color: #bb915e;
            font-weight: bold;

        }
        &-valor{
            width: 65%;
            font-size: 10px;
            display: flex;
            flex-direction: row;
            justify-content: flex-start;
            align-items: center;
            color: white;

            
        }
}
.descripcion{
          width: 100%;
          background-color: #ababab;
  
}
</style>