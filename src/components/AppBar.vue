<template>
    <v-app-bar app>
      <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      <v-toolbar-title>My Application</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn text v-bind="attrs" v-on="on">
            <v-icon left>mdi-account</v-icon>
            Usuario
            <v-icon right>mdi-chevron-down</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item @click="logout">
            <v-list-item-title>Cerrar Sesión</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </template>
  
  <script>
  import { inject } from 'vue'
  import { useRouter } from 'vue-router'
  
  export default {
    setup() {
      const drawer = inject('drawer');
      const router = useRouter();
      
      const toggleDrawer = () => {
        drawer.value = !drawer.value;
      };
  
      const logout = () => {
        router.push({ name: 'Login' });
      };
  
      return { toggleDrawer, logout };
    }
  }
  </script>
  
  <style>
  /* Agrega estilos personalizados si es necesario */
  </style>
  