<script lang="ts" setup >
import {ref} from "vue";
import Parent from "./components/Parent.vue";

let msg = ref(0)
const add = () => {
  msg.value++
}
</script>

<template>
  {{ msg }}
  <button @click="add">+</button><br />
  <parent />
  这是主页面
</template>

<style scoped>
</style>
