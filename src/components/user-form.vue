<script lang="ts" setup>
import { ref } from 'vue'

// Define reactive state for form fields
const firstName = ref('')
const lastName = ref('')
const submitted = ref(false)
const user = ref<{ firstName: string; lastName: string } | null>(null)

// Form submission handler
const handleSubmit = () => {
  if (firstName.value && lastName.value) {
    user.value = {
      firstName: firstName.value,
      lastName: lastName.value
    }
    submitted.value = true
  }
}

// Reset form
const resetForm = () => {
  firstName.value = ''
  lastName.value = ''
  submitted.value = false
  user.value = null
}
</script>

<template>
  <div class="user-form">
    <div class="user-form__overlay"></div>
    <div class="user-form__content">
      <h2 class="user-form__title">Formulario de Usuario</h2>
      
      <form @submit.prevent="handleSubmit" class="user-form__form" v-if="!submitted">
        <div class="user-form__field">
          <label for="first-name" class="user-form__label">Nombre:</label>
          <input
            id="first-name"
            v-model="firstName"
            type="text"
            class="user-form__input"
            required
            placeholder="Ingresa tu nombre"
          />
        </div>
        
        <div class="user-form__field">
          <label for="last-name" class="user-form__label">Apellido:</label>
          <input
            id="last-name"
            v-model="lastName"
            type="text"
            class="user-form__input"
            required
            placeholder="Ingresa tu apellido"
          />
        </div>
        
        <button type="submit" class="user-form__button user-form__button--submit">
          Enviar
        </button>
      </form>
      
      <div class="user-form__result" v-if="submitted && user">
        <h3 class="user-form__subtitle">¡Formulario enviado!</h3>
        <p class="user-form__text">
          Nombre completo: <strong>{{ user.firstName }} {{ user.lastName }}</strong>
        </p>
        <button 
          @click="resetForm" 
          class="user-form__button user-form__button--reset"
        >
          Nuevo formulario
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.user-form {
  max-width: 500px;
  margin: 2rem auto;
  padding: 2rem;
  border-radius: 8px;
  background-image: url('../assets/norwegian-landscape.jpg');
  background-size: cover;
  background-position: center;
  position: relative;
  color: white;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
  overflow: hidden;
}

.user-form__overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, 
    rgba(66, 184, 131, 0.85), 
    rgba(100, 161, 189, 0.75), 
    rgba(53, 73, 94, 0.8));
  z-index: 1;
}

.user-form__content {
  position: relative;
  z-index: 2;
}

.user-form__title {
  color: white;
  margin-bottom: 1.5rem;
  text-align: center;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

.user-form__subtitle {
  color: white;
  margin-bottom: 1rem;
  text-shadow: 0 2px 3px rgba(0, 0, 0, 0.3);
}

.user-form__form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.user-form__field {
  display: flex;
  flex-direction: column;
  text-align: left;
}

.user-form__label {
  margin-bottom: 0.5rem;
  font-weight: 600;
  color: white;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.4);
}

.user-form__input {
  padding: 0.75rem;
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 4px;
  font-size: 1rem;
  background-color: rgba(255, 255, 255, 0.9);
  transition: all 0.3s ease;
}

.user-form__input:focus {
  outline: none;
  border-color: var(--primary-color);
  box-shadow: 0 0 0 3px rgba(66, 184, 131, 0.3);
  background-color: white;
}

.user-form__button {
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 4px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
  margin-top: 0.5rem;
}

.user-form__button--submit {
  background-color: var(--primary-color);
  color: white;
}

.user-form__button--submit:hover {
  background-color: #3aa876;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

.user-form__button--reset {
  background-color: var(--secondary-color);
  color: white;
}

.user-form__button--reset:hover {
  background-color: #2c3d50;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15);
}

.user-form__result {
  text-align: center;
  background-color: rgba(255, 255, 255, 0.2);
  padding: 1.5rem;
  border-radius: 6px;
  backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.user-form__text {
  margin-bottom: 1.5rem;
  font-size: 1.1rem;
  color: white;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
}
</style>
