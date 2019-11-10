<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <span class="mr-2">DWH TEAM</span>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <!-- <Dashboard /> -->
      <Roster  />
    </v-content>
  </v-app>
</template>

<script>
import Dashboard from './components/Dashboard';
import Roster from './components/Roster'

export default {
  name: 'App',

  components: {
    Dashboard,
    Roster
  },

  data: () => ({
    //
  }),
};
</script>
