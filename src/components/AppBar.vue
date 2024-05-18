<template>
    <v-app-bar app>
      <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>
      <v-toolbar-title>My Application</v-toolbar-title>
    </v-app-bar>
  </template>
  
  <script>
  import { inject } from 'vue'
  
  export default {
    setup() {
      const drawer = inject('drawer');
  
      const toggleDrawer = () => {
        drawer.value = !drawer.value;
      };
  
      return { toggleDrawer };
    }
  }
  </script>
  