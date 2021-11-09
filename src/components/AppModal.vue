<template>
  <!-- Background -->
  <div
  @click.self="$emit('close')"
  class="fixed w-full h-full bg-red-600 flex justify-center pt-[10rem] cursor-pointer">
    <!-- Content -->
    <div class="w-[30rem] h-[30rem] bg-light-100 cursor-default shadow-lg">
      <slot name="validator"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    isOpen: {
      type: Boolean,
      required: true,
      default: false,
    },
  },
};
</script>

<style lang="scss" scoped></style>
