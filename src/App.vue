<template>
  <v-app>
    <main__bar/>
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

  data() {
    return {
    }
  },
};
</script>
