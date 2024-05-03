<script setup>
import { reactive, ref } from 'vue'

const awesome = ref(true) 
const count = ref(1)
const text = ref('')


function increment(){
  count.value++
}

function towel() {
  awesome.value = !awesome.value
}


</script>

<template>
  <input v-model="text" placeholder="type here">
    <p>{{ text }}</p>
      <button @click="towel">towel</button>
      <h4>
      <button @click="increment">token: {{ count }}</button>
      </h4>
    <h1 v-if="awesome">saya mengaku menang</h1>
    <h1 v-else>saya mengaku kalah</h1>
</template>


