<template>
  <h1>Car Composition</h1>
  <p>Marca: {{ marca }}</p>
  <p>Modelo: {{ modelo }}</p>
  <p>Potencia: {{ potencia }} C.V</p>
  <button @click="upPower(15)">Aumentar</button><br>
  <button @click="downPower(10)">Disminuir</button>
 
</template>

<script>
import { ref } from 'vue'
export default {
 
  setup() {
    const marca = "Ford";
    const modelo = "B-max";
    let potencia = ref(40);

    const upPower = (newPower) => {
      console.log("Aumentando potencia");
      potencia.value = potencia.value + newPower;
    };

    const downPower = (newPower) => {
      console.log("Disminuyendo potencia");
      potencia.value = potencia.value - newPower;
    };

    return {
      marca,
      modelo,
      potencia,
      upPower,
      downPower
    }
  }
}
</script>

<style>

</style>