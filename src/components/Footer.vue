<script>
  import { store } from '../assets/data/store';

  export default{
    data(){
      return{
        store
      }
    }
  }

</script>

<template>
  
  <h2> heho </h2>
  <button @click="store.counter++" class="btn btn-primary">incrementa</button>

</template>

<style lang="scss" scoped>

</style>