<template>
  <div>
    <router-view />
  </div>
 <Footer />
</template>

<script>

import Footer from './components/Footer.vue'


export default {
  name: 'App',
  components: {


    Footer,
  }

}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;500;600;700;800&family=Libre+Baskerville:wght@400;700&display=swap');
  #app {
    font-family: 'EB Garamond', serif;
    /* font-family: 'Libre Baskerville', serif; */
    border: none;
    margin: 0;
    padding: 0px;
    box-shadow: none;
  }

  a {
    text-decoration: none;
  }

</style>
