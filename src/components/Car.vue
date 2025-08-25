<template lang="">
  <div>
    <h2>一辆{{ car.brand }}车,价值{{ car.price }}万元</h2>
    <button @click="changePrice">涨价10万</button>
  </div>
</template>
<script lang="ts">
export default { name: 'Car' }
</script>

<script setup lang="ts">
import { ref } from 'vue'
import { reactive } from 'vue'
let car = reactive({ brand: '特斯拉', price: 30.5 })

function changePrice() {
  car.price += 10
}
</script>
<style lang=""></style>
