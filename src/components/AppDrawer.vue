<template>
    <v-navigation-drawer v-model="drawer" app>
      <v-list>
        <v-list-item-group>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            @click="navigateTo(item.route)"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </template>
  
  <script>
  import { inject } from 'vue'
  
  export default {
    setup() {
      const drawer = inject('drawer');
      const items = [
        { title: 'Dashboard', icon: 'mdi-view-dashboard', route: '/dashboard' },
        { title: 'Profile', icon: 'mdi-account', route: '/profile' },
        // Agrega más ítems según sea necesario
      ];
  
      const navigateTo = (route) => {
        drawer.value = false;  // Cierra el menú después de navegar
        this.$router.push(route);
      };
  
      return { drawer, items, navigateTo };
    }
  }
  </script>
  