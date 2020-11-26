<template>
  <v-app>
    <Navbar/>
    <v-main id="main_1">
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

<style>
#main_1{
  background:#f0f0f0;
}
</style>