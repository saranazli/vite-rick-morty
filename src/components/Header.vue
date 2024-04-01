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
  
  <h2> {{ store.title }} </h2>

</template>

<style lang="scss" scoped>

h2{
  color: blue;
}

</style>