<template>
  <v-app>
    <SideNav/>

    <v-content>
      <v-container>

          <MainPage/>

      </v-container>
    </v-content>

  </v-app>
</template>

<script>
import MainPage from './components/MainPage.vue';
import SideNav from './components/SideNav.vue';

export default {
  name: 'App',

  components: {
    SideNav,
    MainPage,
  },

  data: () => ({
    //
  }),
};
</script>
