<template>
  <div class="flex space-x-4 items-center justify-center">
    <div
        class="flex flex-wrap w-[250px] h-[180px] items-center justify-center">
      <div class="flex w-full">
        <ButtonBase color="symbol" value="C" @buttonClicked="fnClear"/>
        <ButtonBase color="symbol" value="(" @buttonClicked="fn"/>
        <ButtonBase color="symbol" value=")" @buttonClicked="fn"/>
        <ButtonBase color="operation" value="/" @buttonClicked="fn"/>
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
        class="flex flex-col justify-between w-[280px] h-[180px] items-start justify-start space-y-1 bg-grayscale-white rounded border border-grayblue-15 cursor-pointer text-base"
    >
      <p class="p-6">{{data}}</p>
      <div
          class="border border-grayblue-15 bg-grayblue-5 w-full h-10 flex items-center pl-2 text-grayblue-70">= {{result}}</div>

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
      data: '',
      result: ''
    }
  },
  methods: {
    fn(value) {
      this.data += value
      this.addVal(this.data)
    },

    addVal(values) {
      this.result = eval(values)
    },
    fnClear() {
      this.data = ''
      this.result = ''
    }
  },

}
</script>

<style scoped>

</style>