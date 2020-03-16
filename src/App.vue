<template>
  <v-app>
    <Sidebar/>
    <v-content>
      <Home/>
    </v-content>
  </v-app>
</template>

<script>
import Home from './components/Home.vue';
import Sidebar from './components/Sidebar.vue';

export default {
  name: 'App',

  components: {
    Sidebar,
    Home,
  },

  data: () => ({
    //
  }),
};
</script>
