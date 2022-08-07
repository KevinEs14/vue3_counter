<script>
export default{
  data(){
    //por defecto este metodo necesita retornar un objeto de Js y dentro de este vienen todos los valores de las variables
    return {
      contador: 10,
    } 
  },
  // data:()=>({contador: 10,})
  methods:{
    incrementar(){
      this.contador++;//porque contador esta dentro del objeto. Todo lo que esta dentro de data es un objeto y por eso sus metodos forman parte de ello
    },
    decrementar(){
      this.contador--;
    },
    reset(){
      this.contador=10;
    },
  }
}
  const number = 10;

</script>

<template>
  <div class="container">
    <img src="./assets/logo.svg" alt="logo vue" width="125" height="125" />
    <small>
      <h1>Hola mundo desde Vue</h1>
    </small>
    <hr />
    <h2>Contador: {{contador}}</h2>

    <button @click="incrementar()">+1</button>
    <button @click="decrementar()">-1</button>
    <button @click="reset()">Reset</button>
  </div>
</template>

<style scoped>
/* @import "./assets/base.css"; para importar un modulo*/ 
  .container {
    text-align: center;
    /* background-color:#ddd; */
  }
  small {
    color: #666;
  }
  h1{
    font-weight: bolder;
  }
  h2{
    font-size: 2.5rem;
  }
  button {
    cursor: pointer; /*para pasar por encima y que cambie el color */
    font-size: 1.5rem;
    margin: 0px 6px;
  }
</style>