<template>
  <v-navigation-drawer
    app
    class="text-center"
    permanent
    v-model="drawer"
  >
    <v-list-item>
      <v-list-item-content>
        <v-icon color="primary" size="75">mdi-coffee-outline</v-icon>
        <v-list-item-title class="display-1 font-weight-bold">
          Wilson Chai
        </v-list-item-title>
        <v-list-item-subtitle>
          Software Developer
        </v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>

    <v-list
      nav
      class="d-flex flex-column align-center"
    >
        <v-list-item
          v-for="item in items"
          :key="item"
          link
          class="px-6"
        >
          <v-list-item-content>
            <v-list-item-title>{{ item }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
    </v-list>

    <v-footer
      app
      fixed
      padless
      absolute
    >
      <v-layout
        justify-center
      >
        <v-flex>
          <v-card
            class="text-center"
          >

            <v-card-text class="pb-1">
              <v-btn
                v-for="icon in icons"
                :key="icon"
                icon
              >
                <v-icon size="32">{{ icon }}</v-icon>
              </v-btn>
            </v-card-text>

            <v-card-text class="pt-1">
              &copy; {{ new Date().getFullYear() }} Wilson Chai
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-footer>

  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'SideNav',

  data: () => ({
    drawer: true,
    items: [
      'About',
      'Services',
      'Experience',
      'Skills & Education',
      'Portfolio',
      'Clients',
      'Contact',
    ],
    right: null,
    icons: [
      'mdi-email',
      'mdi-linkedin',
      'mdi-github',
      'mdi-facebook',
    ],
  }),
};
</script>
