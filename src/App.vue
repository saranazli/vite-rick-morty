<script>

  import axios from 'axios';
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';

  export default {

    components: {

      Main,
      Footer

    },
    methods:{
      getApi(){
        console.log('get api');
      }
    },
    mounted(){
      this.getApi()
    }
  }

</script>

<template>
  
  <Main />

  <Footer />

</template>

<style lang="scss" scoped>

  @use './assets/scss/main.scss';

</style>
