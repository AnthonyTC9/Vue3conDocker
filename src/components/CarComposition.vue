<template>
  <h2>Coche - Composition API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower(20)">Aumentar</button>
  <button @click="downPower()">Disminuir</button>
</template>

<script>
import {ref} from "vue";
export default {

    setup(){
        const brand = "Audi";
        const model = "A4";
        let power = ref(40);

        const upPower = (newPower) => {
            //console.log("Aumentar potencia...");
            //power.value++;
            power.value = power.value + newPower;
            //console.log(power.value);
            //power++;            
        };
        const downPower = (newPower) => {
            //console.log("Bajar potencia..." + newPower);
            power.value--;
        }

        return{
            brand,
            model,
            power,
            upPower,
            downPower,
        };
    },

};
</script>

<style>

</style>