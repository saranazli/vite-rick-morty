<script>

  import axios from 'axios';
  import Main from './components/Main.vue';
  import Header from './components/Header.vue';
  import { store } from './assets/data/store';

  export default {

    components: {

      Header,
      Main

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
  
  <Header />
  
  <Main />

</template>

<style lang="scss" scoped>

  @use './assets/scss/main.scss';

</style>
