<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-height: 150px;
  width: 100%;
  padding: 2rem;
  max-width: 1024px;
  margin: auto;
}

nav {
  display: flex;
  gap: 20px;
}

nav a {
  font-size: large;
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  padding: 5px;
}
</style>
