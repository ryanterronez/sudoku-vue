<script setup>
import Box from "./Box.vue";
const props = defineProps(["boxValues"]);
</script>

<template>
  <tr class="top">
    <td v-for="i in 3"><Box :boxValue="i" /></td>
  </tr>
  <tr>
    <td v-for="j in 3"><Box :boxValue="j + 3" /></td>
  </tr>
  <tr class="bottom">
    <td v-for="k in 3"><Box :boxValue="k + 6" /></td>
  </tr>
</template>

<style scoped>
.top {
  border-top: 3px solid black;
}

tr {
  border-left: 3px solid black;
  border-right: 3px solid black;
}

.bottom {
  border-bottom: 3px solid black;
}
</style>
