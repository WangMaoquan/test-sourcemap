<script setup lang="ts">
  import { ref } from 'vue';
  const count = ref(1);
  const add = () => {
    count.value++;
  };
  const add2 = () => {
    throw Error('11');
  };
</script>

<template>
  <div>
    <h1>{{ count }}</h1>
    <div><button @click="add">add</button></div>
    <div><button @click="add2">error</button></div>
  </div>
</template>

<style scoped></style>
