<script setup>
import { ref } from 'vue'

const dice = ref()
let sides = ref()

function roll() {
  dice.value = Math.floor(Math.random() * Math.floor(sides.value)) + 1;
  console.log(dice.value)
}

function restart() {
  dice.value = 0
  sides.value = 0
}

</script>

<template>
  <form @submit.prevent="roll()" class="FormStyle">
    <input v-model="sides" placeholder="Number of sides"/>
    <button>Roll {{ sides }}</button>
  </form>
  <span class="SpanText">You've rolled </span><span class="RolledText">{{ dice }}</span>
  <button @click.prevent="restart">Reset</button>
</template>

<style scoped>
.FormStyle {
  margin-top: 1rem;
  margin-bottom: 1rem;
}
.RolledText {
  padding: .25em 1em;
  background-color: cornsilk;
  font-weight: 600;
  margin-left: .2rem;
  margin-right: .6rem;
}
</style>
