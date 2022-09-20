<template>
  <button
      :class="`button button__${color}`" @click="onClick">
    {{value}}
  </button>
</template>

<script>
import './style.sass'

export default {
  name: "ButtonBase",
  props: {
    color: {
      type: String,
      default: 'number',
      validator(value) {
        return ['number', 'operation', 'zero', 'point', 'symbol']
      }
    },
    value: ''
  },
  methods: {
    onClick() {
      this.$emit("buttonClicked", this.value)
    }
  }
}
</script>

<style scoped>

</style>