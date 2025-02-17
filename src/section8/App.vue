<script setup>
import { ref, useTemplateRef, onMounted } from 'vue'
import CountUp from './CountUp.vue'
const isShow = ref(true)
const userInput = useTemplateRef('user-input')
console.log(userInput.value)
onMounted(() => {
  console.log(userInput.value)
})
</script>
<template>
  <button @click="isShow = !isShow">switch</button>
  <CountUp v-if="isShow" />
  <p><input ref="user-input" type="text" /></p>
</template>
