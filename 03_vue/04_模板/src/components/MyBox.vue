
<!--
 * @Author: chengxy666 425247833@qq.com
 * @Date: 2023-05-27 11:21:00
 * @LastEditors: chengxy666 425247833@qq.com
 * @LastEditTime: 2023-05-27 16:11:17
 * @FilePath: /vue-course/03_vue/04_模板/src/components/MyBox.vue
-->

<script setup></script>
<template>
  <!-- <h1>MyBox</h1> -->

  <!-- <div>
    <h1>MyBox</h1>
    <div class="box1">我是MyBox中的box1</div>
  </div> -->

  <!-- <div></div> -->

  <!-- <div>
    <h2>我是MyBox组件</h2>
  </div> -->

  <div :class="$style.box1">
    <h2>我是MyBox组件</h2>
  </div>
</template>


<style module>
  .box1 {
    background: hotpink;
  }
</style>
