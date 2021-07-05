<template>
  <h1>Car Composition</h1>
  <p>Marca: {{ marca }}</p>
  <p>Modelo: {{ modelo }}</p>
  <p>Potencia {{ potencia }}</p>
  <button @click="upPower(10)">Aumentar potencia</button><br>
  <button @click="downPower(10)">decrementar potencia</button>
</template>


<script>
export default {
    props: {
        potencia: {
            type: Number,
            default: 20
        },

        upPower: Function,
    },

 
    setup(props) {
        const marca = "Ford";
        const modelo = "B-max";

        return {
            marca,
            modelo,
        };
    },
};

</script>

<style>

</style>