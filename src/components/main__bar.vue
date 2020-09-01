<template>
  <v-app-bar app flat color="#ffffff" light>
    <div class="d-flex align-center">
      <div class="mx-auto">
        <v-icon large color="#ff0000">mdi-youtube</v-icon>
        <span class="ml-2">VueTube</span>
      </div>
    </div>
    <v-spacer></v-spacer>
    <div class="my-auto mt-2">
      <v-text-field
        v-model="message4"
        flat
        width="30"
        outlined
        clear-icon
        dense
        clearable
        append-icon="mdi-magnify"
      ></v-text-field>
    </div>
    <v-spacer></v-spacer>

    <div>
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
      <v-avatar class="ml-3">
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
    </div>
  </v-app-bar>
</template>

<script>
export default {};
</script>

<style>
</style>