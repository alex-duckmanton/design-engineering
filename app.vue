<script setup>
import { ref } from 'vue'

const states = ['state-1', 'state-2', 'state-3']
const currentState = ref('')

function randomizeState() {
  var newVal = states[Math.floor(Math.random() * states.length)]

  if (newVal === currentState.value) newVal = false

  currentState.value = newVal
}
</script>

<template>
  <div class="container">
    <div :class="['blob', currentState]"></div>
    <button @click="randomizeState">I'm a button</button>
  </div>
</template>

<style>
@import "~/assets/css/main.css";
</style>

