<template>
  <div class="card-group g-4 p-2">

      <div class="card">
          <img class="card-img-top p-2" :src="details.poster" :alt="details.title">
      <h5 class="card-title text-center">
          {{ details.title }}
      </h5>
      
      <div class="card-text text-center">{{ details.author }}
          <div class="card-text text-center"> {{ details.year }}</div>
      </div>
      </div>

  </div>
</template>

<script>
export default {
    name: 'music',
    props: ["details"]
}
</script>

<style lang="scss" >
    img {
        width: 200px;

    }
</style>

// {
//   "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
//   "title": "New Jersey",
//   "author": "Bon Jovi",
//   "genre": "Rock",
//   "year": "1988"
// },