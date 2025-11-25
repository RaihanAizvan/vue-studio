<script setup>
import { ref } from 'vue'

const count = ref(0)

function inc() {
  count.value++
}
function dec() {
  count.value--
}
</script>

<template>
  <h1>Count: {{ count }}</h1>

  <!-- Conditional rendering -->
  <p v-if="count > 5">Count is greater than 5</p>
  <p v-else-if="count === 5">Count is exactly 5</p>
  <p v-else>Count is less than 5</p>

  <button @click="inc">Increment</button>
  <button @click="dec">Decrement</button>
</template>
