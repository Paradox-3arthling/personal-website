<template>
    <span>
        <v-app-bar app dark :color="nav_bar_color">
            <v-app-bar-nav-icon @click="drawer = true" class="hidden-md-and-up"></v-app-bar-nav-icon>
            <v-spacer class="hidden-md-and-up"/>

            <v-toolbar-title>{{website_title}}</v-toolbar-title>

            <v-spacer class="hidden-sm-and-down"/>
            <template v-for="(item, index) in items">
                <v-btn :key="index" v-bind:to="item.href" text class="hidden-sm-and-down"> {{ item.text }} </v-btn>
            </template>
            <v-spacer class="hidden-sm-and-down"/>
        </v-app-bar> 
        <v-navigation-drawer app :color="nav_bar_color" dark v-model="drawer" disable-resize-watcher temporary class="hidden-md-and-up">
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
        website_title: String,
        nav_bar_color: String
    }
}
</script>