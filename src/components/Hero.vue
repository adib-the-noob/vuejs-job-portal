<script setup>
const props = defineProps({
  title: {
    type: String,
    default: "Become a Vue.js Developer!",
  }, subTitle: {
    type: String,
    default: "Find the best jobs!",
  }
});
</script>

<template>
  <!-- Hero -->
  <section class="bg-[#006A71] py-20 mb-4">
    <div
        class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col items-center"
    >
      <div class="text-center">
        <h1
            class="text-4xl font-extrabold text-[#F2EFE7] sm:text-5xl md:text-6xl"
        >
          {{ props.title }}
        </h1>
        <p class="my-4 text-xl text-[#F2EFE7]">
          {{ props.subTitle }}
        </p>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>