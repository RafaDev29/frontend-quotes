<template>
  <div class="flex h-screen">
    <!-- Formulario de inicio de sesión -->
    <div class="w-full h-screen flex justify-center items-center bg-gray-800">
      <LoginForm />
    </div>

    <!-- Imagen -->
   
  </div>
</template>



<script>
import LoginForm from './views/LoginForm'

export default {
  name: 'App',
  components: {
    LoginForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 100px;
}

/* Estilos adicionales para hacer que la imagen ocupe la mitad de la pantalla */
.bg-cover {
  width: 100%;
  height: 100%;
}
</style>
