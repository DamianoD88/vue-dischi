<template>
  <section>
      <div class="row" v-if="!loading">
          <div v-for="(music, index) in album" :key="index" class="col-6 col-md-4 col-lg-3">
              {{ music.title  }}
              <!-- <music :details="music" /> -->
          </div>
      </div>
      <!-- <Loader v-else ladel="Vue-dischi" /> -->
      <!-- <Song /> -->
  </section>
</template>

<script>
import axios from 'axios';
// import Loader from '@/components/Loader.vue';
// import Song from '@/components/Song.vue';


export default {
    name: 'Album',
    components: {
        // Song,
        // Loader
    },
    data() {
        return {
            apiURL : 'https://flynn.boolean.careers/exercises/api/array/music',
            album : '',
            loading: true
        }
    },
    created(){
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
                    this.loading = false;
                })
                .catch(error => {
                    console.log('Errore: ', error);
                })
        }
    }
}
</script>

<style lang="scss" scoped>

</style>