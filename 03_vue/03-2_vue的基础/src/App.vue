<!--
 * @Author: chengxy666 425247833@qq.com
 * @Date: 2023-05-23 10:29:13
 * @LastEditors: chengxy666 425247833@qq.com
 * @LastEditTime: 2023-05-23 12:18:50
 * @FilePath: /vue-course/03_vue/04_vue的基础/src/App.vue
-->

<template>
  <div>
    <h1>演示组合API🥸</h1>
    <h2 @click="fn">{{ count }}</h2>
  </div>
</template>

<script setup>
import { reactive, ref } from "vue";
import { $ref } from 'vue/macros'; // 虽然避免弹出警告但是也可以不用引入
/**
 * reactive()
 *    - 返回一个对象的响应式代理
 *    - 返回的是一个深层响应式对象
 *    - 也可以使用shallowReactive()创建一个浅层响应式对象
 *    - 缺点：
 *      - 只能返回对象的响应式代理, 不能处理原始值
 * ref()
 *    - 接收一个任意值，并返回它的响应式代理
 * ref 原理：
 *    - ref在生成响应式代理时，它是将值包装为了一个对象 0 --> {value: 0}
 *    - 访问ref对象时，必须通过 对象.value 来访问其中的值
 *    - 在模版中，ref对象会被自动解包
 *
 * vue 给我们提供了一个语法糖，使得ref对象在script标签中也可以自动解包
 * $是一个实验性的，需要在vite插件中做一些配置 reactivityTransform: true
 */

const stu = reactive({
  name: '程续缘yyds'
})

// count = 10; // 改变量只会影响到变量自己，在js中，无法实现对一个变量的代理
// const count = 0; // 原始值
// const count = ref(0); // 生成一个0的响应式代理

// let count = ref(0); // 生成一个0的响应式代理
// console.log(count.value);
// function fn() {
//   // count自增
//   count.value++;
// }

let count = $ref(0); // 生成一个0的响应式代理
console.log(count);

function fn() {
  // count自增
  count++;
}


</script>