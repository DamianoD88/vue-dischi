<template>
  <div id="app">
    <Header message="App di vue-dischi"/>
    <Album />
    
    
  </div>
</template>

<script>
import Header from '@/components/Header.vue';
import Album from '@/components/Album.vue';

export default {
  name: 'App',
  components: {
    Header,
    Album
  }
}
</script>

<style lang="scss">
@import '@/style/general.scss';
#app{
  background-color: #1e2d3b;
}
</style>
