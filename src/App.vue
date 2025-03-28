<script lang="ts" setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

const title = ref('Hola Mundo con Vue 3!')
</script>

<template>
  <div class="app">
    <header class="app__header">
      <img 
        alt="Vue logo" 
        class="app__logo" 
        src="https://vuejs.org/images/logo.png" 
        width="125" 
        height="125" 
      />
      <h1 class="app__title">{{ title }}</h1>
    </header>
    <main>
      <HelloWorld />
    </main>
  </div>
</template>

<style scoped>
:root {
  --primary-color: #42b883;
  --secondary-color: #35495e;
  --text-color: #2c3e50;
  --spacing-base: 1rem;
}

.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: var(--text-color);
  margin-top: var(--spacing-base);
}

.app__header {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: var(--spacing-base);
}

.app__logo {
  margin-bottom: var(--spacing-base);
}

.app__title {
  font-size: 2rem;
  color: var(--primary-color);
}
</style>