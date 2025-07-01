<script setup>
import { reactive } from 'vue'

// 定义 props
defineProps({
  msg: {
    type: String,
    required: true,
  },
})

// 使用 reactive 定义响应式对象
const mydata = reactive({
  id: 1,
  name: "张宇航",
  age: 18,
  sex: "男",
  address: "中国",
})
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>

    <!-- 显示 mydata 的内容 -->
    <div>姓名：{{ mydata.name }}</div>
    <div>年龄：{{ mydata.age }}</div>
    <div>地址：{{ mydata.address }}</div>

    <!-- 更新按钮示例 -->
    <button @click="mydata.name = '张佳琳'">更新姓名</button>

    <h3>
      您已成功创建了一个项目，包含
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> 和
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {

  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
