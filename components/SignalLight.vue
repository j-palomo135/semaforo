<template>
    <div :style="{ backgroundColor: color }" class="light" :class="{ active: isActive }"></div>
  </template>
  
  <script setup>
  defineProps({
    color: String,
    isActive: Boolean
  });
  </script>
  
  <style scoped>
  .light {
    width: 50px;
    height: 50px;
    margin: 8px 0;
    border-radius: 50%;
    opacity: 0.3;
    transition: opacity 0.3s;
  }
  .light.active {
    opacity: 1;
  }
  </style>
  