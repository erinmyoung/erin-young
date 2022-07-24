<script setup>
import { RouterLink, RouterView } from "vue-router";
import Header from "./components/Header.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
      <Header />
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  min-height: var(--header-height);
  display: flex;
  justify-content: center;
  align-content: center;
  width: 100vw;
  background-image: linear-gradient(to bottom right,#08929c,#8f0561);
}

.wrapper {
  display: grid;
  grid-template-columns: repeat(2, auto);
  width: 100%;
  padding: 2rem 0;
}

nav {
  font-size: 16px;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  color: var(--color-text-hover);
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

nav, .details {
  display: block;
  margin: auto;
}

.details {
  font-size: 45px;
}
</style>
