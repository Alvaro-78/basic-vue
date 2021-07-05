<template>
  <CarComposition />
  <hr>
  <CarOptions />
  <Car :potencia="potencia" :upPower="upPower" :downPower="downPower" />
</template>

<script>
import { ref } from 'vue';
import CarComposition from './components/CarComposition.vue';
import CarOptions from './components/CarOptions.vue';
import Car from './components/Car.vue';
export default {
  components: {
    CarComposition,
    CarOptions,
    Car
  },
  setup() {
    let potencia = ref(40);

    const upPower = newPower => {
      potencia.value = potencia.value + newPower;
    };

    const downPower = newPower => {
      potencia.value = potencia.value - newPower;
    };

    return {
      potencia,
      upPower,
      downPower
    };
  },
};
</script>

<style>

</style>