<template>
    <div class="page-container">
      
      <h1 class="title">SEMÁFORO</h1>
  
      
      <SignalController />
    </div>
  </template>
  
  <script setup>
  import SignalController from '~/components/SignalController.vue';
  </script>
  
  <style scoped>
  
  .page-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
    gap: 20px;
  }

  .title {
    font-size: 24px;
    font-weight: bold;
    color: #333;
    text-align: center;
    margin-bottom: 20px;
  }
  </style>
  