
<script>
export default {
  props:{
    name: String,
    status: String,
    species:String,
    image: String,
  }
}
</script>

<template>
  <div class="col mb-3">
    <div class="mt-3">
      <img :src="image" class="card-img-top" :alt="name">
      <div>
        <h3>{{ name }}</h3>
        <p>{{ status }}</p>
        <p>{{ species }}</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>