<template>
<div>
  <v-app-bar app flat color="#ffffff" light>
    <v-layout row wrap align-center>
      <v-btn icon @click="drawer = !drawer">
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      <div class="d-flex align-center">
        <div class="mx-auto">
          <v-icon large color="#ff0000">mdi-youtube</v-icon>
          <span class="ml-2">VueTube</span>
        </div>
      </div>
      <v-spacer></v-spacer>
      <v-flex class>
        <v-text-field
          flat
          hide-details
          placeholder="Search"
          outlined
          dense
          append-icon="mdi-magnify"
        ></v-text-field>
      </v-flex>
      <v-spacer></v-spacer>

      <v-flex md2>
        <v-btn icon>
          <v-icon>mdi-video-plus</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-apps</v-icon>
        </v-btn>
        <v-btn icon>
          <v-badge content="9" color="red" overlap>
            <v-icon>mdi-bell</v-icon>
          </v-badge>
        </v-btn>
        <v-avatar class="ml-3" size="32px">
          <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
        </v-avatar>
      </v-flex>
    </v-layout>
  </v-app-bar>

  <v-navigation-drawer
      app
      v-model="drawer"
      width="80px"
      mini-variant
      mini-variant-width="100"
      class="align-center"
    >
      <v-list>
        <v-list-item class="mb-4" justify-center>
        </v-list-item>
        <v-list-item v-for="i in drawer__icons" :key="i.name">
          <v-list-item-content>
            <v-icon class="mb-1">{{i.icon}}</v-icon>
            <v-list-item-subtitle class="caption" align="center">{{i.name}}</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    </div>
</template>

<script>
export default {
  data() {
    return{
      drawer: false,
      drawer__icons: [
      { name: "Home", icon: "mdi-home" },
      { name: "Trending", icon: "mdi-fire" },
      { name: "Subscriptions", icon: "mdi-youtube-subscription" },
      { name: "Library", icon: "mdi-play-box-multiple" },
    ]
    }
  },
};
</script>

<style>
</style>