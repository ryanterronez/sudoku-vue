<script setup>
import Box from "./Box.vue";
defineProps({
  boxValues: Array,
  rowNumber: String
});
</script>

<template>
  <table>
    <tbody>
      <tr>
        <td
          class="top"
          :class="index % 3 === 0 ? 'left' : ''"
          v-if="rowNumber % 3 === 0"
          v-for="(boxValue, index) in boxValues"
        >
          <Box :boxValue="boxValue" />
        </td>
        <td
          class="middle"
          :class="index % 3 === 0 ? 'left' : ''"
          v-else
          v-for="(boxValue, index) in boxValues"
        >
          <Box :boxValue="boxValue" />
        </td>
      </tr>
    </tbody>
  </table>
</template>

<style scoped>
.top {
  border-top: 5px solid black;
}
.middle {
  border-top: 1px solid black;
}
.left {
  border-left: 3px solid black;
}
td {
  padding-top: 0px;
  padding-bottom: 0px;
}
table {
  border-spacing: 0px;
}
</style>
