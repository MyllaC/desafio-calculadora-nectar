<template>
  <div class="flex space-x-2 items-center justify-center">
    <div
        class="flex flex-wrap w-[250px] h-[180px] items-center justify-center">
      <div class="flex w-full">
        <ButtonBase color="symbol" value="C" @buttonClicked="fnDelete"/>
        <ButtonBase color="symbol" value="(" @buttonClicked="fn"/>
        <ButtonBase color="symbol" value=")" @buttonClicked="fn"/>
        <ButtonBase color="operation" value="+" @buttonClicked="fn"/>
      </div>
      <div class="flex w-full">
        <ButtonBase value="7" @buttonClicked="fn"/>
        <ButtonBase value="8" @buttonClicked="fn"/>
        <ButtonBase value="9" @buttonClicked="fn"/>
        <ButtonBase color="operation" value="*" @buttonClicked="fn"/>
      </div>
      <div class="flex w-full">
        <ButtonBase value="4" @buttonClicked="fn"/>
        <ButtonBase value="5" @buttonClicked="fn"/>
        <ButtonBase value="6" @buttonClicked="fn"/>
        <ButtonBase color="operation" value="-" @buttonClicked="fn"/>
      </div>
      <div class="flex w-full">
        <ButtonBase value="1" @buttonClicked="fn"/>
        <ButtonBase value="2" @buttonClicked="fn"/>
        <ButtonBase value="3" @buttonClicked="fn"/>
        <ButtonBase color="operation" value="+" @buttonClicked="fn"/>
      </div>
      <div class="flex w-full">
        <ButtonBase color="zero" value="0" @buttonClicked="fn"/>
        <ButtonBase color="point" value="." @buttonClicked="fn"/>
      </div>
    </div>
    <div
        class="flex flex-wrap w-[280px] h-[180px] items-start justify-start space-y-1 p-10 bg-grayscale-white rounded text-grayblue-70 border border-grayblue-15 cursor-pointer text-base"
    >
      {{inputValue}}
      <span>= {{result}}</span>
    </div>
  </div>

</template>

<script>
import ButtonBase from "./Buttons/ButtonBase.vue";

export default {
  name: "Calculator",
  components: {ButtonBase},
  data() {
    return {
      inputValue: [],
      result: ''
    }
  },
  methods: {
    fn(value) {
      this.inputValue.push(parseInt(value))
      this.calculator()
    },
    fnDelete() {
      this.inputValue = []
    },
    calculator() {
      const initialValue = 0;

      this.result = this.inputValue.reduce(
          (previousValue, currentValue) => previousValue +
              currentValue,
          initialValue)
    }
  }
}
</script>

<style scoped>

</style>