<script setup>
  const props = defineProps({
    bg: {
      type: String,
      default: "bg-gray-100"
    }
  })
</script>

<template>
  <div :class="`${props.bg} p-6 rounded-lg shadow-md text-black`" >
    <slot></slot>
  </div>
</template>

<style scoped>

</style>