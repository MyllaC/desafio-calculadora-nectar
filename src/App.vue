<template>

  <div
      class="w-screen h-screen bg-grayscale-5 flex items-center justify-center">
    <Calculator />
  </div>

</template>

<script>
import './assets/tailwind.css'


import Calculator from "./components/Calculator.vue";

export default {
  components: {Calculator}
}


</script>

