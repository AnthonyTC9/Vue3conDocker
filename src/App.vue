<template>
  <h1>Vue JS</h1>
 <!-- <CarOptions />
  <hr />
  <CarComposition />-->
  <!-- :upPower se usa para props y el @downPower se usa para emits-->
  <Car3 :power="power" :upPower="upPower" @downPower="downPower"/>
</template>

<script>
import { ref } from "vue";
//import CarComposition from "./components/CarComposition"
//import CarOptions from "./components/CarOptions"
import Car3 from "./components/Car3"

export default {
  components:{
    //CarComposition,
    //CarOptions,
    Car3,
  },
  //el setup es para props
  setup(){
    let power = ref(36);

    const upPower = () => {
      //console.log("Aumentar power...");
      power.value++;
    };

    const downPower = () => {
      power.value--;
    };

    return {
      power,
      upPower,
      downPower,
    };
  },

};
</script>

<style>

</style>
