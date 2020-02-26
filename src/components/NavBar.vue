<template>
    <span>
        <span class="hidden-md-and-up">
            <v-app-bar app dark color="grey darken-3">
                <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
                <v-spacer/>
                <v-toolbar-title>{{appTitle}} </v-toolbar-title>
            </v-app-bar> 
            <v-navigation-drawer app v-model="drawer" disable-resize-watcher temporary>
                <v-list nav>
                    <template v-for="(item, index) in items">
                        <v-list-item :key="index" v-bind:to="item.href" link>
                            <v-list-item-content> {{ item.text }} </v-list-item-content>
                        </v-list-item>
                        <v-divider :key="index"/>
                    </template>
                </v-list>
            </v-navigation-drawer>
        </span> 
        <!-- will add a crumb menu for medium up devices -->
        
        <v-app-bar app dark class="hidden-sm-and-down" color="grey darken-3">
            <v-toolbar-title> {{appTitle}} </v-toolbar-title>
            <v-spacer/>
                <template v-for="(item, index) in items">
                    <v-btn :key="index" v-bind:to="item.href" text> {{ item.text }} </v-btn>
                </template>
            <v-spacer/>
        </v-app-bar>
        <!-- <v-container fluid class="hidden-sm-and-down grey darken-3">
            <v-row justify="center">
                <v-col cols="auto">
                    <v-breadcrumbs :items="items" divider="-" large></v-breadcrumbs>
                </v-col>
            </v-row>
        </v-container> -->
    </span> 
</template>

<script>
export default {
    name: "NavBar",
    data: () => ({
        drawer: false,
        items: [
          {text: 'HOME', href: '/'},
          {text: 'ABOUT ME', href: '/about'}
        ]
    }),
    props: {
        appTitle: String
    }
}
</script>