<template>
  <v-app>
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
    width: 80%;
  }
</style>
