<script>

  import axios from 'axios';
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';
  import { store } from './assets/data/store';

  export default {

    components: {

      Main,
      Footer

    },
    data(){
      return{
        store
      }
    },
    methods:{
      getApi(){
        console.log('get api');
        axios.get(this.store.apiUrl, {
          params:{
            
          num: 25,
          offset: 0,
          language:'it'

          }
        })
        .then( result => {
          console.log(result.data)
        })
        .catch( error => {
          console.log(error)
        })
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
