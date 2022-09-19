<template>

  <div class="w-screen h-screen bg-gray-400 flex items-center justify-center">
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

