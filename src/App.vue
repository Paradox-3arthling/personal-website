<template>
  <v-app>
    <NavBar :appTitle="user_s_name" />
    <v-content>
      <router-view></router-view>
    </v-content>
    <Footer :user_s_name="user_s_name"/>
  </v-app>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "App",
  components: {
    NavBar,
    Footer
  },
  data: () => ({
    user_s_name: "Paradox-3arthling" // set ur name to be used in SPA
  })
};
</script>
