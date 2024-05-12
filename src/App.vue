<script setup>
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div id="layout">
    <header>
      <div class="wrapper">
        <nav>
          <RouterLink :to="{name: 'event-list'}">Events</RouterLink>
          <RouterLink :to="{name: 'about'}">About</RouterLink>
        </nav>
      </div>
    </header>
  </div>
<!--ini yang akan mengubah view berdasarkan route-->
  <RouterView />
</template>

<style>
header {
  line-height: 1.5;
  max-height: 100vh;
}

#layout {
  font-family: Avenir, "Helvetica Neue", Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
}

nav a {
  text-decoration: none;
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

p{
  font-size: 20px;
}
</style>
