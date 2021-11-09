<template>
  <div
  v-if="!isOpen" 
  class="w-full flex justify-center mt-[10rem]">
    <button
      @click="isOpen = true"
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
  <AppModal v-if="isOpen" :isOpen="isOpen" @close="isOpen = false">
    <template v-slot:validator>
      <AppModalValidator :validPhrase="validPhrase"/>
    </template>
  </AppModal>
</template>

<script>
import AppModal from "@/components/AppModal.vue";
import AppModalValidator from "@/components/AppModalValidator.vue";


export default {
  components: {
    AppModal,
    AppModalValidator
  },
  name: "App",
  data() {
    return {
      isOpen: false,
      validPhrase: 'my password',
    };
  },
};
</script>

<style lang="scss" scoped></style>
