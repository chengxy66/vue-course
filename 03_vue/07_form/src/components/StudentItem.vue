<!--
 * @Author: chengxy666 425247833@qq.com
 * @Date: 2023-06-05 12:18:46
 * @LastEditors: chengxy666 425247833@qq.com
 * @LastEditTime: 2023-06-05 16:00:57
 * @FilePath: /vue-course/03_vue/07_form/src/components/StudentItem.vue
-->

<script setup>

import { inject } from 'vue';

// const props = defineProps(['students']);
// const emits = defineEmits(['delStu']);

// const name = inject('name');
// console.log(name);

// const msg = inject('msg');
// console.log(msg);

const { students, delStu } = inject('student');

// 定义一个删除学生的方法
const delStuHandler = (index) => {
  if (confirm('该操作不可恢复，请确认')) {
    // emits('delStu', index);
    delStu(index);
  }
}

</script>

<template>
  <tbody>
    <!-- <tr v-for="(stu, index) in props.students" :key="stu.id"> -->
    <tr v-for="(stu, index) in students" :key="stu.id">
      <td>{{ stu.id }}</td>
      <td>{{ stu.name }}</td>
      <td>{{ stu.age }}</td>
      <td>{{ stu.gender }}</td>
      <td>{{ stu.address }}</td>
      <!-- <td><a href="javascript:;" @click.prevent="delStuHandler(index)">删除</a></td> -->
      <td><a href="javascript:;" @click.prevent="delStuHandler(index)">删除</a></td>
    </tr>
  </tbody>
</template>

<style scoped>
td {
  border: 1px solid;
  font-size: 24px;
}
</style>