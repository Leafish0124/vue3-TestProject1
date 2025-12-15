<template>
  <div class="about">
    <h2>关于我们</h2>
  </div>
</template>

<script lang="ts">
export default {
  name: 'about',
}
</script>

<script setup lang="ts">
import { ref, reactive, computed } from 'vue'
import {onMounted, onUnmounted} from 'vue'

onMounted(() => {
  console.log('About组件挂载完成')
})

onUnmounted(() => {
  console.log('About组件卸载完成')
})

const props = defineProps<{
  prop: string
}>()

const emits = defineEmits(['event'])

</script>

<style scoped>
.about {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  color: rgb(85, 84, 84);
  font-size: 18px;
}
</style>