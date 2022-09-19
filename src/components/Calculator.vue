<template>
  <div
      class="flex flex-wrap w-[300px] items-center justify-center space-y-1 ">
    <div class="flex space-x-1 w-[200px]">
      <ButtonBase>
        C
      </ButtonBase>
      <ButtonBase>
        (
      </ButtonBase>
      <ButtonBase>
        )
      </ButtonBase>
      <ButtonBase>
        +
      </ButtonBase>
    </div>
    <div class="flex space-x-1 w-[200px]">
      <ButtonBase>
        7
      </ButtonBase>
      <ButtonBase>
        8
      </ButtonBase>
      <ButtonBase>
        9
      </ButtonBase>
      <ButtonBase>
        *
      </ButtonBase>
    </div>
    <div class="flex space-x-1 w-[200px]">
      <ButtonBase>
        4
      </ButtonBase>
      <ButtonBase>
        5
      </ButtonBase>
      <ButtonBase>
        6
      </ButtonBase>
      <ButtonBase>
        -
      </ButtonBase>
    </div>
    <div class="flex space-x-1 w-[200px]">
      <ButtonBase>
        1
      </ButtonBase>
      <ButtonBase>
        2
      </ButtonBase>
      <ButtonBase>
        3
      </ButtonBase>
      <ButtonBase>
        +
      </ButtonBase>
    </div>
    <div class="flex space-x-1 w-[200px]">
      <button class="grow border border-blue-500 rounded text-grayblue-50 bg-grayscale-white border border-grayblue-10">
        0
      </button>
      <button class="w-[46.5px] border border-blue-500 rounded text-grayblue-50 bg-grayscale-white border border-grayblue-10">
        .
      </button>
    </div>
  </div>
</template>

<script>
import ButtonBase from "./Buttons/ButtonBase.vue";
export default {
  name: "Calculator",
  components: {ButtonBase}
}
</script>

<style scoped>

</style>