<template>
  <v-app>
    <NavBar appTitle="Floyd's Website"/>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import NavBar from "@/components/NavBar.vue";

export default {
  name: "App",
  components: {
    NavBar
  }
};
</script>
