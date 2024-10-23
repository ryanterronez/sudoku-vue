<script setup>
import NumberChooser from "./components/NumberChooser.vue";
import Board from "./components/Board.vue";
</script>

<template>
  <div class="app-container">
    <Board />
    <NumberChooser />
  </div>
</template>

<style scoped>
.app-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
