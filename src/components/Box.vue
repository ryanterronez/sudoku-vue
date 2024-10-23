<script setup>
const props = defineProps(["boxValue"]);
</script>

<template>
  <button>{{ boxValue }}</button>
</template>

<style scoped>
button {
  font: comic sans ms;
  font-size: 32px;
  width: 80px;
  /* Adjust size as needed */
  height: 80px;
  /* Adjust size as needed */
  border-radius: 0;
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: grey;
}
</style>
