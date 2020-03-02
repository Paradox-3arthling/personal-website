<template>
  <v-app>
    <NavBar :appTitle="website_title" />
    <v-content>
      <router-view></router-view>
    </v-content>
    <Footer :user_s_name="footer_name"/>
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
    website_title: "Floyd",          // set the name to be displayed in the navigation bar
    footer_name: "Paradox-3arthling" // set the name to be displayed in the footer
  })
};
</script>
