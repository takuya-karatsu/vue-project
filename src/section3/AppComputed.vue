<script setup>
import { ref, computed } from 'vue'
const score = ref(0)
const count = ref(0)
function tmp() {
  // console.log('tmp')
  return score.value > 3 ? 'Good' : 'Bad'
}
const evaluation = computed(() => {
  console.log('computed')
  return score.value > 3 ? 'Good' : 'Bad'
})
function getEvaluation() {
  console.log(evaluation.value)
}
</script>
<template>
  <p>{{ score > 3 ? 'Good' : 'Bad' }}</p>
  <p>{{ tmp() }}</p>
  <p>score: {{ score }}</p>
  <p>count: {{ count }}</p>
  <button @click="score++">score +1</button>
  <button @click="count++">count +1</button>
  <button @click="getEvaluation">get Evaluation</button>
</template>
