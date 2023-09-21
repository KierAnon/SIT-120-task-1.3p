<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div id="app-container">
    <header>
      <div class="wrapper">
        <nav>
          <RouterLink class="nav-link" to="/">Home</RouterLink>
          <RouterLink class="nav-link" to="/resume">Resume</RouterLink>
          <RouterLink class="nav-link" to="/about">About</RouterLink>
        </nav>
      </div>
    </header>

    <RouterView />
  </div>
</template>

<style>
/* Overall app container */
#app-container {
  font-family: 'Arial', sans-serif;
}

/* Wrapper for centered content */
.wrapper {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Styles for the header */
header {
  background-color: #f7f7f9;
  padding: 15px 0;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-link {
  padding: 10px 20px;
  margin: 0 10px;
  text-decoration: none;
  color: #333;
  border-radius: 5px;
  transition: background-color 0.3s ease, color 0.3s ease;

  &:hover {
    background-color: #e0e0e4;
    color: #000;
  }

  /* Active link styling - if using vue-router's active class */
  &.router-link-active {
    background-color: #d1d1d6;
    color: #000;
  }
}

/* Responsive adjustments for smaller screens */
@media (max-width: 768px) {
  nav {
    flex-direction: column;
  }

  .nav-link {
    margin: 5px 0;
  }
}
</style>