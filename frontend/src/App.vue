<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class=""

          src="@/assets/wolves_wide.png"
          transition="scale-transition"
          width="80"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn class="mr-3" color="secondary" to="/">
        <v-icon >mdi-scoreboard-outline</v-icon>
      </v-btn>
      <v-btn class="mr-3" color="secondary" to="/console">
        <v-icon >mdi-console</v-icon>
      </v-btn>
      <span class="mr-2 text-h4">{{ this.date }}</span>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    date: new Date().toLocaleDateString("de-DE", {year: "numeric", month: "long", day: "numeric"})
  }),

};
</script>

<style>
  html {
    overflow-y: auto !important;
  }
</style>
