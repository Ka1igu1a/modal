<template>
  <div class="w-full flex justify-center mt-[10rem]">
    <button
      @click="isOpen = true"
      v-if="!isOpen"
      class="
        border
        rounded-full
        border-blue-700
        text-blue-700
        hover:shadow-lg
        p-[1rem]
        focus:outline-none
      "
    >
      Open modal
    </button>
  </div>
  <AppModal v-if="isOpen" :isOpen="isOpen" @aa="isOpen = false" />
</template>

<script>
import AppModal from "@/components/AppModal.vue";

export default {
  components: {
    AppModal,
  },
  name: "App",
  data() {
    return {
      isOpen: false,
    };
  },
};
</script>

<style lang="scss"></style>
