<template>
  <div>{{ msg }}</div>
</template>

<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
/* Add any styles here if needed */
</style>
