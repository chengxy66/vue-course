<!--
 * @Author: chengxy666 425247833@qq.com
 * @Date: 2023-05-29 15:39:12
 * @LastEditors: chengxy666 425247833@qq.com
 * @LastEditTime: 2023-05-30 10:32:57
 * @FilePath: /vue-course/03_vue/06_props/src/01_props.vue
-->

<script setup>
import MyBox from './components/MyBox.vue';
import { ref } from 'vue';

// const count = ref(0);
const obj = ref({
  count: 0
});

</script>

<template>
  <div>
    <h1>我是父组件</h1>
    <!-- <MyBox a="111" /> -->
    <!-- <MyBox a="111" b="33333" /> -->
    <!-- <MyBox :count="count" :obj="obj" maxLength="100" /> -->
    <!-- <MyBox :count="count" :obj="obj" max-length="100" /> -->
    <!-- <MyBox :count="'123'" :obj="obj" max-length="100" /> -->
    <!-- <MyBox :count="123" :obj="obj" /> -->
    <!-- <MyBox :count="123" :obj="obj" maxLength="嘻嘻嘻"/> -->
    <!-- <MyBox :count="123" :obj="obj" maxLength="1111"/> -->
    <!-- <MyBox :count="123" :obj="obj" maxLength="1111" isCheck/> -->
    <MyBox :count="123" :obj="obj" maxLength="1111"/>
    <button @click="obj.count++">点我一下</button>
  </div>
</template>