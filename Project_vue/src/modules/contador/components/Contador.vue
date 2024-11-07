<template>
  <h1>Hello World</h1>
  
  <p>{{count}}</p>
  <button @click="incrementar">Increment</button>
  <button @click="decrementar">Decrement</button>

</template>

<script setup>
import {ref} from "vue";
const count = ref(0);
const incrementar=() => {
  count.value++
}
const decrementar=() => {
  count.value--
}
</script>

<style scoped>
p {
  color: red;
}

</style>
