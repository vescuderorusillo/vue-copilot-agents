<script lang="ts" setup>
import { ref } from 'vue'

const message = ref('¡Bienvenido a tu aplicación Vue.js usando Composition API!')
const count = ref(0)

const increment = () => {
  count.value++
}
</script>

<template>
  <div class="hello-world">
    <p class="hello-world__message">{{ message }}</p>
    <div class="hello-world__counter">
      <p>Has hecho click {{ count }} veces</p>
      <button class="hello-world__button" @click="increment">Incrementar</button>
    </div>
  </div>
</template>

<style scoped>
.hello-world {
  margin: 2rem auto;
  max-width: 600px;
}

.hello-world__message {
  font-size: 1.2rem;
  margin-bottom: 2rem;
  color: var(--secondary-color);
}

.hello-world__counter {
  padding: 1.5rem;
  border-radius: 8px;
  background-color: #f8f8f8;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.hello-world__button {
  margin-top: 1rem;
  padding: 0.5rem 1.5rem;
  background-color: var(--primary-color);
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
  transition: background-color 0.3s;
}

.hello-world__button:hover {
  background-color: #3aa876;
}
</style>