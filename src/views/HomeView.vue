<script setup>
import { storeToRefs } from 'pinia';
import { useCounter } from '@/stores/counter';
import HelloWorld from '@/components/HelloWorld.vue';

const counter = useCounter();

const { count, doubleCount } = storeToRefs(counter);
const { increment } = counter;

const add = () => {
  increment();
};
</script>

<template>
  <HelloWorld :msg="'vue'"></HelloWorld>
  <button @click="add">点击</button>
  <div>{{ count }} * 2 = {{ doubleCount }}</div>
</template>
<style scoped></style>
