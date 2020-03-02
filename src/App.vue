<template>
  <v-app>
    <NavBar :website_title="website_title" />
    <v-content>
      <router-view></router-view>
    </v-content>
    <Footer :footer_name="footer_name"/>
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
    website_title: "Floyd",               // set the name to be displayed in the navigation bar
    footer_name: "Paradox-3arthling",     // set the name to be displayed in the footer
    nav_and_footer_color: "grey darken-3" // set the color for the navigation and footer centrally from here
  })
};
</script>
