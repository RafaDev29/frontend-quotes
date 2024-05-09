<template>
  <div class="flex flex-col md:flex-row h-screen">
    <!-- Formulario de inicio de sesión -->
    <div class="md:w-4/5 flex justify-center items-center bg-orange-500">
      <form class="bg-white p-8 rounded-lg shadow-md w-full max-w-lg">
        <h2 class="text-3xl font-semibold mb-6 text-center">Iniciar sesión</h2>
        <div class="mb-6">
          <label for="email" class="block text-gray-700 font-semibold mb-2">Correo electrónico</label>
          <input type="email" id="email" v-model="email" class="w-full border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:border-blue-500">
        </div>
        <div class="mb-6">
          <label for="password" class="block text-gray-700 font-semibold mb-2">Contraseña</label>
          <input type="password" id="password" v-model="password" class="w-full border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:border-blue-500">
        </div>
        <button type="submit" class="w-full bg-blue-500 text-white font-semibold py-2 px-4 rounded-md hover:bg-blue-600">Iniciar sesión</button>
      </form>
    </div>

    <!-- Imagen -->
    <div class="md:w-1/3 bg-orange-500 bg-cover bg-center"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    handleSubmit(event) {
      event.preventDefault();
      // Aquí puedes agregar la lógica para enviar los datos de inicio de sesión al servidor
      console.log('Correo electrónico:', this.email);
      console.log('Contraseña:', this.password);
    }
  }
}
</script>

<style scoped>
form {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
}

input {
  border-width: 1px;
}

button {
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #3182ce;
}

/* Estilos adicionales para el formulario */
form {
  border-radius: 10px;
}

input[type="email"],
input[type="password"] {
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 10px;
  margin-bottom: 10px;
}

button {
  border: none;
  outline: none;
  cursor: pointer;
}

/* Estilos para el contenedor de la imagen */
.md\:w-1\/3 {
  width: 39.333333%;
}
</style>
