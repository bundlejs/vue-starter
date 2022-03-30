<script setup>
defineProps({
  msg: {
    type: String,
    default: '',
  },
});
</script>

<template>
  <div>
    <div>hello {{ msg }}</div>
  </div>
</template>

<style scoped></style>
