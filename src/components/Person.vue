<template>
  <div class="person">
    <h2>当前求和为：{{ sum }}</h2>
    <button @click = "add">+1</button>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Person',
}
</script>

<script setup lang="ts">
import { reactive, ref, toRefs } from 'vue'
let sum = ref(0);

function add() {
  sum.value++;
}
</script setup>

<style scoped>
.person {
  background-color: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}

button {
  margin: 5px;
}
</style>
