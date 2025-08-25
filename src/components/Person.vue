<template>
  <div class="person">
    <h2>姓名：{{ person.name }}</h2>
    <h2>年龄：{{ person.age }}</h2>
    <input v-model="name" placeholder="输入新姓名" />
    <button @click="changeName">修改姓名</button>
    <input v-model="age" type="number" placeholder="输入新年龄" />
    <button @click="changeAge">修改年龄</button>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Person',
}
</script>

<script setup lang="ts">
import { reactive, ref, toRefs } from 'vue'
let person = reactive({
  name: '张三',
  age: 18,
  newName: String(''),
  newAge: Number(0)
})
let { name, age } = toRefs(person)
let newName = toRefs(person)

function changeName() {
  name.value += '~'
}
function changeAge() {
  age.value += 1
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
