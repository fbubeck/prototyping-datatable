<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >

    </v-app-bar>

    <v-main>
      <div id="app">
      <img src="./assets/Vue App Header.png" class="center">
      </div>
      <Datatable/>
    </v-main>
  </v-app>
</template>

<script>
import Datatable from './components/datatable.vue';

export default {
  name: 'App',

  components: {
    Datatable,
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="css">
  .center {
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
  }
</style>
