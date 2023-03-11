<script lang="ts" setup>
import { ref } from 'vue'
import Child from "./Child.vue";

let count = ref(0)
const add = () => {
  count.value++
}
</script>

<template>
  <child :count="count"/>
  这是父页面<br />
  <button @click="add">+</button><br />


</template>

<style scoped>
</style>
