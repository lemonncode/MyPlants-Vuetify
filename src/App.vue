<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6"> Mis plantitas </v-list-item-title>
          <v-list-item-subtitle> no olvidar darles amor! </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" :to="item.to" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color="primary" dark src="monstera.png" height="170xp">
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
        ></v-img>
      </template>
      <v-container class="pa-0">
        <v-row>
          <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
          <v-spacer></v-spacer>
          <search />
        </v-row>
        <v-row>
          <v-toolbar-title class="text-h4 ml-4">Mis plantitas</v-toolbar-title>
        </v-row>
        <v-row>
          <livedatetime />
        </v-row>
      </v-container>
    </v-app-bar>

    <v-main>
      <!--  -->
      <router-view></router-view>
      <snackbar />
    </v-main>
  </v-app>
</template>

<script>
import Search from "./components/Tools/Search.vue";
import LiveDateTime from "./components/Tools/LiveDateTime.vue";
import Snackbar from "@/components/Globo/Snackbar.vue";

export default {
  data: () => ({
    drawer: null,
    items: [
      { title: "Mis Plantitas", icon: "mdi-flower-tulip-outline", to: "/" },

      { title: "Sobre mí", icon: "mdi-account-heart-outline", to: "/about" },
    ],
  }),
  components: {
    search: Search,
    livedatetime: LiveDateTime,
    snackbar: Snackbar,
  },
};
</script>

