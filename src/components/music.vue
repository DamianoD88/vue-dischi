<template>
  <div>
      <img :src="details.poster" :alt="details.title">
      <div>{{ details.author }}
          <div> {{ details.year }}</div>
      </div>
      
  </div>
</template>

<script>
export default {
    name: 'music',
    props: ["details"]
}
</script>

<style>

</style>

// {
//   "poster": "https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg",
//   "title": "New Jersey",
//   "author": "Bon Jovi",
//   "genre": "Rock",
//   "year": "1988"
// },