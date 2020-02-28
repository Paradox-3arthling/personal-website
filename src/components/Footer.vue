<template>
    <v-footer height="auto" color="grey darken-3" dark>
        <v-container>
            <v-row>
                <v-col v >
                    <p> &copy;{{ current_year }}. Powered by Vue </p>
                    <!-- <router-link to="/about"> Made by {{ user_s_name }} </router-link> -->
                    <a href="https://github.com/Paradox-3arthling"> Made by {{ user_s_name }} </a>
                </v-col>
            </v-row>
        </v-container>
    </v-footer>
</template>
<script>
export default {
    name: "Footer",
    data: () => ({
        current_year: (new Date()).getFullYear()
    }),
    props: {
        user_s_name: String
    }
}
</script>
<style scoped>
    p, a {
        text-decoration: none;
        margin-left: 5%;
        font-size: 12px;
    }
    .v-footer {
        padding: 0px;
    }
    .container {
        padding: 0.1%;
    }
    .v-application p {
        margin-bottom: 0px;
    }
</style>