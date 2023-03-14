<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer">
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/men/78.jpg"
        title="John Leider"
      ></v-list-item>

      <v-divider></v-divider>

      <v-list density="compact" nav>
        <v-list-item
          prepend-icon="mdi-account-circle-outline"
          to="/dashboard"
          title="Accounts"
          value="home"
        ></v-list-item>
        <!-- <v-list-item
          prepend-icon="mdi-forum"
          title="About"
          value="about"
        ></v-list-item> -->
      </v-list>
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <RouterView />
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: null,
  }),
};
</script>