<template>
  <Car />
  <hr>
  <Car2 />
</template>

<script>
import Car from './components/CarComposition.vue'
import Car2 from './components/CarOptions.vue'
export default {
  components: {
    Car,
    Car2
  }
}
</script>

<style>

</style>