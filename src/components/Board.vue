<script setup>
import { ref } from "vue";
import Square from "./Square.vue";

const board = ref(new Array(9).fill(new Array(9).fill(0)));
const solution = ref([]);

async function getBoard() {
  const url = "https://sudoku-api.vercel.app/api/dosuku";
  try {
    const response = await fetch(url);
    if (!response.ok) {
      throw new Error(`Response status: ${response.status}`);
    }
    const json = await response.json();
    board.value = json.newboard.grids[0].value;
    solution.value = json.newboard.grids[0].solution;
  } catch (error) {
    console.error(error.message);
  }
}
</script>

<template>
  <button @click="getBoard">Board</button>
  <table>
    <tr v-for="i in 3">
      <td v-for="j in 3">
        <Square />
      </td>
    </tr>
  </table>
</template>

<style scoped>
button {
  font: comic sans ms;
  font-size: 32px;
  width: 100px;
  height: 80px;
  border-radius: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: grey;
}
</style>
