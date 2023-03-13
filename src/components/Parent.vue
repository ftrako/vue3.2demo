<script lang="ts" setup>
import { ref } from 'vue'
import Child from "./Child.vue";

let count = ref(0)
const add = () => {
  count.value++
}

const handleClick = (data:number) => {
  console.log("Parent->handleClick: " + data)
}
</script>

<template>
  <child :age="10" :count="count" @handleClick="handleClick"/>
  这是父页面<br />
  <button @click="add">+</button><br />


</template>

<style scoped>
</style>
