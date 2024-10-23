<script setup>
import Row from "./Row.vue";
</script>

<template>
  <Row class="top" :boxValues="[1, 2, 3, 4, 5, 6, 7, 8, 9]" />
</template>

<style scoped>
.top {
  border-top: 5px solid black;
  padding-top: 20px;
}
</style>
