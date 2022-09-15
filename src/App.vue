<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="wrapper">
    <header>
      <nav>
      <h1>Dice Roller</h1>
        <router-link to="/" class="navText">Home</router-link>
        <router-link to="/about" class="navText">About</router-link>
      </nav>
    </header>

    <RouterView/>
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
}
header {
  line-height: 1.5;
  max-height: 100vh;
  justify-content: space-between;
  font-size: 1.5rem;
}

.navText {
  padding-inline: 1em;
  font-size: 1rem;
}

nav {
  width: 100%;
  text-align: center;
  margin-top: 2rem;
}

nav a:first-of-type {
  border: 0;
}
</style>
