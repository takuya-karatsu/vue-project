<script setup>
import { ref } from 'vue'
const count = ref(0)
</script>
<template>
  <p>{{ $attrs }}</p>
  <h2 v-bind="$attrs">CountUp</h2>
  <BaseIcon />
  <p class="red">count:{{ count }}</p>
  <button @click="count++">button</button>
</template>
