<template>
  <Person />
</template>

<script>
export default {
  name: 'App',
  components: {
    Person,
  },
}
</script>

<script setup>
import Person from './components/Person.vue';

let isShow = true;
</script>

<style scoped>
.app {
  background-color: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>
