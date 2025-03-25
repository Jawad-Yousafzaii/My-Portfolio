<template>
    <div class="bubble-container">
      <div class="bubble relative overflow-hidden">
        <slot></slot>
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .bubble-container {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 1rem;
  }
  
  .bubble {
    background: white;
    clip-path: ellipse(70% 50% at 50% 50%);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    width: 300px; /* Adjust size as needed */
    height: 200px; /* Adjust size as needed */
  }
  </style>
  