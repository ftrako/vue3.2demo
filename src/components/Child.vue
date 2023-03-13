<script lang="ts" setup>

// 老的写法
// defineProps({
//   count: Number
// })

// // 新写法
// defineProps<{
//   count: number
// }>()

// 新写法带默认值
withDefaults(defineProps<{
  count: number
  age: number
}>(),{age:100})

const emits = defineEmits<{(e : 'handleClick', data:number):void}>()

const modify = () => {
  console.log("Child->modify")
  emits("handleClick",22)
}


</script>

<template>
  这是子页面 count={{ count }}<br/>
  这是子页面 age={{ age }}<br/>
  <button @click="modify">子页面修改按钮</button>
  <br/>
</template>

<style scoped>
</style>
