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
  background: url('assets/art-header.png') center no-repeat;
  width: 100vw;
  height: 100%;
  display: flex;
}

.wrapper {
  display: grid;
  grid-template-columns: repeat(2, auto);
  align-self: center;
  margin: auto;
  width: 100%;
  max-width: 80%;
  height: 100%;
  background-color: white;
  padding: 1rem 0;
  position: relative;
}

nav {
  font-size: 18px;
  display: block;
  margin: auto;
}

nav a.router-link-exact-active {
  color: var(--color-accent);
}

nav a.router-link-exact-active:hover {
  color: var(--color-accent-hover);
}

nav a {
  color: var(--color-text);
  display: inline-block;
  font-weight: 500;
  padding: 0 1rem;
  border-left: 2px solid var(--color-border);
}

nav a:hover {
  color: var(--color-accent-hover);
}

nav a:first-of-type {
  border: 0;
}
</style>
