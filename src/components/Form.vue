<template>
  <form @submit.prevent="handleSubmit">
    <div>
      <label for="nome">Nome:</label>
      <input type="text" id="nome" v-model="formData.nome" required />
    </div>
    <div>
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="formData.email" required />
    </div>
    <div>
      <label for="mensagem">Mensagem:</label>
      <textarea id="mensagem" v-model="formData.mensagem" required></textarea>
    </div>
    <button type="submit">Enviar</button>
  </form>
</template>

<script setup>
import { ref } from 'vue';

const formData = ref({
  nome: '',
  email: '',
  mensagem: '',
});

const handleSubmit = () => {
  // Aqui você pode adicionar a lógica para lidar com os dados do formulário
  console.log('Dados do formulário:', formData.value);
  // Por exemplo, você pode enviar os dados para um servidor
};
</script>

<style scoped>
/* Estilos do formulário aqui */
form {
  max-width: 400px;
  margin: 0 auto;
}

label {
  display: block;
  margin-bottom: 5px;
}

input,
textarea {
  width: 100%;
  padding: 8px;
  margin-bottom: 10px;
}

button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>
