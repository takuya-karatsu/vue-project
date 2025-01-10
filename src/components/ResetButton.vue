<script setup>
defineEmits(['resetCount'])
// const emit = defineEmits(['resetCount'])
// function emitReset() {
//   emit('resetCount', 100)
// }
</script>
<template>
  <!-- <button @click="emitReset">Reset</button> -->
  <button @click="$emit('resetCount', 100)">Reset</button>
</template>
