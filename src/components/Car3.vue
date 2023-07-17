<template>
    <h2>Coche - Composition API</h2>
    <p>Marca: {{ brand }}</p>
    <p>Modelo: {{ model }}</p>
    <p>Potencia: {{ power }}</p>
    <button @click="upPower">Aumentar</button>
    <button @click="downPowerFn">Disminuir</button>
  </template>
  
  <script>
  export default {
    props:{
        power: {
            type: Number,
            default: 60,
        },
        upPower: Function,
    },
    emits: ["downPower"],
      setup(props, context){
          const brand = "Audi";
          const model = "A4";

          const downPowerFn = () => {
            context.emit("downPower");
          };
          

         // const testPower = () => {
           // props.upPower();
         // };

  
          return{
              brand,
              model,
            //  testPower,
            downPowerFn,
          };
      },
  
  };
  </script>
  
  <style>
  
  </style>