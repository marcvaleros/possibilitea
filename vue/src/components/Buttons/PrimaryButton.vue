<template>
  <div
    class="
      flex
      justify-center
      items-center
      bg-primary
      rounded-[9px]
      text-textButtons text-buttonText
      font-bold
      hover:cursor-pointer
      text-center
    "
    :class="
      hover != undefined ? `hover:bg-${hover}` : 'hover:bg-primaryHovered'
    "
    :style="{
      height: height + 'px',
      width: width + 'px',
      color: color,
      fontSize: fontSize + 'px',
    }"
  >
    {{ finalText }}
  </div>
</template>

<script>
export default {
  name: "PrimaryButton",
  props: {
    text: String,
    height: Number,
    width: Number,
    fontSize: Number,
    color: String,
    hover: String,
  },
  computed: {
    finalText() {
      return this.text.toUpperCase();
    },
  },
};
</script>

<style scoped>
</style>