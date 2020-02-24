<template>
  <v-app>
    <v-app-bar app dark>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title>{{appTitle}} </v-toolbar-title>
        <v-spacer/>
        <v-btn text to="/">HOME</v-btn>
        <v-btn text to="/about">ABOUT</v-btn>
    </v-app-bar>

    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: "App",

  data: () => ({
    appTitle: 'Floyd\'s website',
    drawer: false
  })
};
</script>
