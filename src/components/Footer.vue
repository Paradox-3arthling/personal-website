<template>
    <v-footer padless dark>
      <v-card
        flat
        tile
        width="100%"
        :color="footer_color"
        class="text-center"
      >
        <v-card-text class="py-1">
          <v-btn
            v-for="icon in icons"
            :key="icon.name"
            class="mx-4"
            icon
            :href="icon.href"
            target="_blank"
          >
            <v-icon size="20px">{{ icon.name }}</v-icon>
          </v-btn>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text py-1" style="font-size:12px;" t>
          &copy;{{ current_year }} — <strong>Vuetify</strong>. Made by {{ footer_name }}.
        </v-card-text>
      </v-card>
    </v-footer>
</template>
<script>
export default {
    name: "Footer",
    data: () => ({
        current_year: (new Date()).getFullYear(),        
        icons: [
            {name: 'fab fa-github-alt', href:'https://github.com/Paradox-3arthling'},
            {name: 'fab fa-twitter', href:'https://twitter.com/Karanja_Baked'},
            {name: 'fab fa-linkedin', href:'https://www.linkedin.com/in/floyd-karanja-413788a9/'},
            {name: 'fab fa-instagram', href:'https://www.instagram.com/parad0x_3arthling'},
        ],
    }),
    props: {
        footer_name: String,
        footer_color: String
    }
}
</script>