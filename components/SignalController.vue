<template>
    <div class="signal-controller">
      <!-- Semáforo -->
      <div class="signal-body">
        <SignalLight color="red" :isActive="currentLight === 'red'" />
        <SignalLight color="yellow" :isActive="currentLight === 'yellow'" />
        <SignalLight color="green" :isActive="currentLight === 'green'" />
      </div>
  
      <!-- Columna de botones al lado derecho del semáforo -->
      <div class="button-column">
        <button @click="changeLight('red')" class="color-button red-button">Rojo</button>
        <button @click="changeLight('yellow')" class="color-button yellow-button">Amarillo</button>
        <button @click="changeLight('green')" class="color-button green-button">Verde</button>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import SignalLight from '~/components/SignalLight.vue';
  
  const currentLight = ref('red'); // Estado inicial
  
  function changeLight(color) {
    currentLight.value = color;
  }
  </script>
  
  <style scoped>
  /* Contenedor principal para centrar el semáforo y botones */
  .signal-controller {
    display: flex;
    align-items: center;
    gap: 20px;
    padding-top: 20px;
    justify-content: center;
  }
  
  /* Contenedor del semáforo */
  .signal-body {
    width: 90px;
    background-color: #222;
    padding: 12px;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
  }
  
  /* Columna de botones fuera del semáforo */
  .button-column {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  
  /* Estilo para los botones */
  .color-button {
    padding: 6px 12px;
    border: none;
    border-radius: 5px;
    font-weight: bold;
    cursor: pointer;
    color: white;
    width: 80px;
    text-align: center;
    transition: transform 0.2s;
  }
  .color-button:hover {
    transform: scale(1.05);
  }
  
  /* Colores específicos para cada botón */
  .red-button {
    background-color: #cc3333;
  }
  .yellow-button {
    background-color: #cccc33;
    color: black;
  }
  .green-button {
    background-color: #33cc33;
  }
  </style>
  