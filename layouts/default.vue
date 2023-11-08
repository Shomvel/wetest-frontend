<template>
    <div class="layout">
      <Navbar />
      <div class="content-container">
        <slot />
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  // Your Vue 3 Composition API code here
  </script>
  
  <style scoped>
  .layout {
    display: flex;
    flex-direction: column;
    height: 100vh; /* Adjust this value based on your needs */
  }
  
  .content-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex-grow: 1; /* This will make the slot container take up the remaining space */
    width: 100%;
    max-width: 1200px; /* Or the max width you want your content to have */
    margin: 0 auto;
  }
  </style>