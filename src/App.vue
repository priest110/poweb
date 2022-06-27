<template>
  <v-app class="background_img">
    <v-main>
      <HomePage/>
    </v-main>
  </v-app>
</template>

<script>
import HomePage from './components/HomePage';

export default {
  name: 'App',

  components: {
    HomePage,
  },

  data: () => ({
  }),

   mounted() {
    document.title = "POWEB";
  }
};
</script>
<style>
.background_img {
  background: url('assets/background.jpg') no-repeat center center fixed !important;
  background-size: 100% 100% !important;
  background-attachment: fixed;
}

</style>