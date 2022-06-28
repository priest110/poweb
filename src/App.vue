<template>
  <v-app class="background_img" :class="$vuetify.breakpoint.xl || $vuetify.breakpoint.lg || $vuetify.breakpoint.md ? '' : ''">
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
  background-size: cover   !important;  
}

</style>