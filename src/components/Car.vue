<template>
  <h2>Coche</h2>
  <p>Marca: {{ brand }}</p>
  <p>modelo: {{ model }}</p>
  <p>Color:
   <!--<span v-for="(color, index) in colors" :key="index">
      {{ index }}:{{ color }} -
    </span>-->
  </p>
  <ul>
    <li  v-for="(color, index) in colors" :key="index">
        {{ index }}:{{ color }} -
    </li>
  </ul>
  <p>precio: {{ precio }}</p>
  <p>power: {{ power }}</p>
  {{ mensaje.title }} - {{ mensaje.text }}
</template>

<script>

export default {

    setup(){
        const brand = "audi";
        const model = "A4";
        const colors = ["azul", "morado", "marron", "amarillo"];
        const price = 45555;
        const power = 240;
        const mensaje = {
            title: "estoy bien",
            text: "welcome",
        }
        return {
            brand,
            model,
            colors,
            price,
            power,
            mensaje,
        };
    },




        /*data(){
        return{
            brand: "Audi",
            model: "A4",
            color: ["Azul", "Rojo", "Verde"],
            precio: 38000,
            power: 190,
            mensaje:{
                title: "hola mundo",
                text: "adios",
            },
        };
    },*/

};
</script>

<style>

</style>