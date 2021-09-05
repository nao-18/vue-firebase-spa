<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-app-bar-title>マイアドレス帳 </v-app-bar-title>
      <v-spacer></v-spacer>
    </v-app-bar>
    <SideNav />

    <v-content></v-content>
  </v-app>
</template>

<script>
import SideNav from "./components/SideNav.vue";

export default {
  name: "App",

  components: {
    SideNav,
  },

  data: () => ({
    //
  }),
};
</script>
