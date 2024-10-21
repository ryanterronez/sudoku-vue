<script setup>
import { ref } from 'vue';

const value = ref('')
</script>

<template>
  <button>{{ value }}</button>
</template>

<style scoped>
button {
  font: comic sans ms;
  font-size: 32px;
  width: 80px; /* Adjust size as needed */
  height: 80px; /* Adjust size as needed */
  border-radius: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: grey;
}
</style>
