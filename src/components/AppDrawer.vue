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
  import { ref } from 'vue'
  import { useRouter } from 'vue-router'
  
  export default {
    setup() {
      const drawer = ref(false);
      const items = [
        { title: 'Home', icon: 'mdi-home', route: '/' },
        { title: 'About', icon: 'mdi-information', route: '/about' },
        // Agrega más ítems según sea necesario
      ];
  
      const router = useRouter();
  
      const navigateTo = (route) => {
        router.push(route);
      };
  
      return { drawer, items, navigateTo };
    }
  }
  </script>
  