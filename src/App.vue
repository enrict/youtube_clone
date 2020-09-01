<template>
  <v-app>
    <main__bar />
    <v-navigation-drawer
      app
      permanent
      width="80px"
      mini-variant
      mini-variant-width="100"
      class="align-center"
    >
      <v-list>
        <v-list-item class="mb-4" justify-center>
          <v-btn icon tile class="mx-auto">
            <v-icon>mdi-menu</v-icon>
          </v-btn>
        </v-list-item>
        <v-list-item v-for="i in drawer__icons" :key="i.name">
          <v-list-item-content>
            <v-icon class="mb-1">{{i.icon}}</v-icon>
            <v-list-item-subtitle class="caption" align="center">{{i.name}}</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import main__bar from "./components/main__bar";

export default {
  name: "App",

  components: {
    main__bar,
  },

  data: () => ({
    drawer: true,
    drawer__icons: [
      { name: "Home", icon: "mdi-home" },
      { name: "Trending", icon: "mdi-fire" },
      { name: "Subscriptions", icon: "mdi-youtube-subscription" },
      { name: "Library", icon: "mdi-play-box-multiple" },
    ],
    nav__icons: [
      { name: "Library", icon: "mdi-home" },
      { name: "History", icon: "mdi-history" },
      { name: "My videos", icon: "mdi-home" },
      { name: "Watch later", icon: "mdi-home" },
    ],
  }),
};
</script>
