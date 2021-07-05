<template>
  <h1>Car Options</h1>
  <p>Marca: {{ marca }}</p>
  <p>Modelo: {{ modelo }}</p>
  <p>Potencia: {{ potencia }}</p>
  <button @click="upPower(10)">Aumentar potencia</button><br>
  <button @click="downPower(5)">Disminuir potencia</button>
 </template>

<script>
export default {
    data() {
        return {
            marca: "Seat",
            modelo: "Ibiza",
            potencia: 80
        };
    },
    methods: {
        upPower(newPower) {
            this.potencia = this.potencia + newPower;
        },
        downPower(newPower) {
           this.potencia = this.potencia - newPower;
        }
    }
}
</script>

<style>

</style>