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
  import { useRouter } from 'vue-router'
  
  export default {
    setup() {
      const drawer = inject('drawer');
      const router = useRouter();
      const items = [
        { title: 'Dashboard', icon: 'mdi-view-dashboard', route: '/dashboard' },
        { title: 'Profile', icon: 'mdi-account', route: '/profile' },
      ];
  
      const navigateTo = (route) => {
        drawer.value = false;
        router.push(route);
      };
  
      return { drawer, items, navigateTo };
    }
  }
  </script>
  