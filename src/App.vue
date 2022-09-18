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

};
</script>
<style>
  .background_img {
    background: url('assets/background.jpg') no-repeat center center fixed !important;
    background-size: cover   !important;  
  }

  @media screen and (min-width:960px) {
    .background_img {
      min-height: 800px;
    }
  }
</style>