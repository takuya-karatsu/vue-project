<script setup>
import { ref, reactive } from 'vue'
// let a = 1
// let b = 2
// let c = a + b // c = 3
// a = 4
// console.log(c)
const title = ref('Vue.js Course')
let price = ref(9.99)
function increment() {
  price.value += 1
  instructor.age += 1
  instructor.sns.twitter = 'hello'
  instructor.email = 'info@example.com'
}
const info = ref({
  students: 1000,
  rating: 4,
})
const instructor = reactive({
  name: 'Yoshipi',
  age: 25,
  sns: {
    twitter: '@__yoshipi__',
    youtube: '@yoshipi',
  },
  email: ref('yoshipi@example.com'),
})
instructor.bio = 'hello'
const items = reactive([ref(1), ref(2), ref(3)])
items.reverse()
const courseInfo = {
  sections: ref(10),
  language: ref('Japanese'),
}
console.log(courseInfo.sections.value)
</script>
<template>
  <h1>Title: {{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
  <h2>students: {{ info.students }}</h2>
  <h2>Instructor age: {{ instructor.age }}</h2>
  <h2>Instructor SNS Twitter: {{ instructor.sns.twitter }}</h2>
  <h2>Instructor email: {{ instructor.email }}</h2>
  <h2>Course Info Sections: {{ courseInfo.sections.value }}</h2>
</template>
