<template>
  <div>
    <div class="absolute top-81 left-1/3 z-60">
      <div class="bg-light-50 w-[25rem] h-[25rem]">sa</div>
    </div>

    <div
      @click="$emit('aa')"
      class="bg-gray-200 w-full h-full absolute top-0 cursor-pointer"
    ></div>
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

<style lang="scss" scoped="scss"></style>
