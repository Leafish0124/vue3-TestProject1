<template>
  <h2 class="title">Vue路由测试</h2>
  <!-- 导航区 -->
  <div class="navigate">
    <RouterLink to="/home" active-class="active">首页</RouterLink> 
    <RouterLink to="/news" active-class="active">新闻</RouterLink>
    <RouterLink to="/about" active-class="active">关于</RouterLink>
  </div>
  <!-- 展示区 -->
  <div class="main-content">
    <RouterView></RouterView>
  </div>
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
import { RouterLink, RouterView } from 'vue-router';

let isShow = true;
</script>

<style scoped>
.title{
  text-align: center;
  word-spacing: 5px;
  margin:30px 0;
  height: 70px;
  line-height: 70px;
  font-size: 36px;
  background-image: linear-gradient(45deg,gray,white);
  border-radius: 10px;
  box-shadow: 0 0 2px ;
}
.navigate{
  display: flex;
  justify-content: space-around;
  margin: 0 100px;
}
.navigate a {
  display: block;
  text-align: center;
  width: 90px;
  height: 40px;
  line-height: 40px;
  border-radius: 10px;
  background-color: gray;
  text-decoration: none;
  color: white;
  font-size: 18px;
  letter-spacing: 5px;
}
.navigate a.active{
  background: color #64967e;
  color: #ffc268;
  font-weight: 900;
  text-shadow: 0 0 1px #000;
  font-family: 微软雅黑;
}
.main-content{
  margin: 0 auto;
  margin-top: 30px;
  height: 400px;
  width: 90%;
  border: 1px solid;
  border-radius: 10px;
  box-shadow: 0 0 5px gray;
}
</style>
