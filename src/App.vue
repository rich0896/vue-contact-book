<script setup>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
<header>
  <h1>Contacts</h1>
  <div class="menu">
    <input type="text" placeholder="Search contacts" />
    <button aria-label="Add Contact">+</button>
  </div>
</header>
<RouterView />
</template>

<style scoped>
header {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 0.5rem 1rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid #444;
  color: white;
}

.menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  /* max-width: 400px; */
}

.menu input {
  padding: 0.5rem;
  border: none;
  border-radius: 0.25rem;
  width: 100%;
  max-width: 800px;
}

.menu button {
  padding: 0.2rem 0.5rem;
  border: none;
  border-radius: 0.25rem;
  background-color: white;
  color: #202020;
  cursor: pointer;
  font-size: larger;
}
</style>
