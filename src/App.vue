<template>
  <v-app>
    <AppBar v-if="showMenu" />
    <AppDrawer v-if="showMenu" />
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import { ref, provide, computed } from 'vue'
import { useRoute } from 'vue-router'
import AppDrawer from './components/AppDrawer.vue'
import AppBar from './components/AppBar.vue'

export default {
  components: {
    AppDrawer,
    AppBar
  },
  setup() {
    const drawer = ref(false);
    provide('drawer', drawer);

    const route = useRoute();
    const showMenu = computed(() => route.name !== 'Login');

    return { drawer, showMenu };
  }
}
</script>

<style>
/* Agrega estilos personalizados si es necesario */
</style>
