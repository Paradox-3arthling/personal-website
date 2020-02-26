<template>
    <span>
        <v-app-bar app dark>
            <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title>{{appTitle}} </v-toolbar-title>
            <v-spacer/>
            <v-btn text to="/">HOME</v-btn>
            <v-btn text to="/about">ABOUT</v-btn>
        </v-app-bar> 
    </span> 
</template>

<script>
export default {
    name: "NavBar",
    data: () => ({
        drawer: false
    }),
    props: {
        appTitle: String
    }
}
</script>