<template>
   <form action="">
        <fieldset>
            <legend>Nombre</legend>
            <label for="Inputnombre">Ingrese su nombre</label>
            <input id="Inputnombre"   type="text" placeholder="Nombre">
        </fieldset>
        <fieldset>
            <legend>Apellido</legend>
            <label for="Inputapellido">Ingrese su apellido</label>
            <input id="Inputapellido"   type="text" placeholder="Apellido">
        </fieldset>
        <fieldset>
            <legend>Edad</legend>
            <label for="Inputedad">Ingresa su edad</label>
            <input id="Inputedad"   type="number" placeholder="NumeroTelefonico" required min="18" max="80"> 
        </fieldset>
        <fieldset class="exepcion">
            <legend>Sexo</legend>
            <label for="InputMasculino">Masculino</label>
            <input id="InputMasculino"  name="sexo" type="radio" checked>
            <label for="InputFemenino">Femenino</label>
            <input id="InputFemenino"  name="sexo" type="radio" checked>
        </fieldset>
        <fieldset>
            <legend>DNI</legend>
            <label for="InputDNI">Ingresa su DNI</label>
            <input id="InputDNI"   type="text" placeholder="Ingrese su DNI" minlength="8" maxlength="8"> 
        </fieldset>
        <fieldset>
            <legend>Correo Electrónico</legend>
            <label for="Inputcorreo">Ingresa su correo electrónico</label>
            <input id="Inputcorreo"   type="email" placeholder="example@gmail.com">
        </fieldset>
        <input type="submit">
    </form>
</template>

<script>

export default {
    
}
</script>

<style scoped lang="scss">
*{
box-sizing: border-box;
padding: 0;
margin:0;
}
legend{
    font-size: 18px;
    color: #bb915e;
}
label{
    font-size: 13px;
}
fieldset{
    width: 100%;
    padding: 0 5% 0 5%;
    margin-bottom: 10px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 50px;
}
label, input{
    display: inline-block;
    width: 200px;
}
.exepcion label, .exepcion input{
    width: 20%;
}
form{
    width: 80%;
    margin: auto;
    border: 2px solid black;
    padding: 2%;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #d2b694;
    background-color: #333333;
}

input:focus{
    color: red
}
</style>