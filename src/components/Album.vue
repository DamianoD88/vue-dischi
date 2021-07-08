<template>
  <section>
      <div class="row">
          <div v-for="music in album" :key="music.title" class="col-6 col-md-4 col-lg-3">
              {{ music.author }}
          </div>
      </div>
  </section>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Album',
    data() {
        return {
            apiURL : 'https://flynn.boolean.careers/exercises/api/array/music',
            album : ''
        }
    },
    axios(){
        this.getAlbum();
    },
    methods: {
        getAlbum(){
            axios
                .get(this.apiURL)
                .then(response => {
                    console.log(response.data);
                    this.Album = response.data;
                    console.log(this.Album);
                })
                .catch(error => {
                    console.log('Errore: ', error);
                })
        }
    }
}
</script>

<style lang="scss">

</style>