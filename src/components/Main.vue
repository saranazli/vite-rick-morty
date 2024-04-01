
<script>

  import { store } from '../assets/data/store';
  import Card from './partials/Card.vue'

  export default{
    components: {
      Card
    },
    data() {
      return{
        store
      }
    }
  }

</script>

<template>
  
  <div class="gen">
    <div class="text-center my-5 container">
      <div class="row row-cols-4">
        <Card 
        v-for=" card in this.store.cards" 
        :key="card.id" 
        :name="card.name"
        :status="card.status"
        :species="card.species"
        :image="card.image "
        />
      </div>
  </div>
  </div>

</template>

<style lang="scss" scoped>

  @use '../assets/scss/main.scss' as*;

  .gen{
    background-color: $bg-color;
  }

</style>