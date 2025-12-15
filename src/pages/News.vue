<template>
  <div class="news">
    <ul>
        <li v-for="item in newsList" :key="item.id">
            <a href="#">{{ item.title }}</a>
        </li>

        <div class="news-content">
            <h2>新闻内容展示区</h2>
            <p>点击左侧新闻标题，显示对应的新闻内容</p>
        </div>
    </ul>
  </div>
</template>

<script lang="ts">
export default {
  name: 'News',
}
</script>

<script setup lang="ts">
import { ref, reactive, computed } from 'vue'

const newsList = reactive([
    { id: 1, title: '新闻001', content: '这是新闻001的内容' },
    { id: 2, title: '新闻002', content: '这是新闻002的内容' },
    { id: 3, title: '新闻003', content: '这是新闻003的内容' },
    { id: 4, title: '新闻004', content: '这是新闻004的内容' },
]);

</script>

<style scoped>
.news {
  padding: 0 20px;
  display: flex;
  /* justify-content: center; */
  height: 100%;
}
.news ul {
  margin-top: 30px;
  list-style: none;
  padding-left: 10px;
}
.news li>a {
    font-size: 10px;
    line-height: 40px;
    text-decoration: none;
    color: #64967E;
    text-shadow: 0 0 1px rgb(0, 84, 0);
}
.news-content{
    width: 70%;
    height: 90%;
    border: 1px solid;
    margin-top: 20px;
    border-radius: 10px;
}
</style>