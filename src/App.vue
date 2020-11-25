<template>
  <v-app>
    <Navbar/>
    <v-main>
      <router-view/>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Navbar from '@/components/Navbar';
import Footer from '@/components/FooterComp.vue';
export default {
  name: 'App',

  components: {
    HelloWorld,
    Navbar,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>