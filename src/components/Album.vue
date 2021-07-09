<template>
  <section>
      <div class="row" v-if="!loading">
          <div v-for="(music, index) in Album" :key="index" class="col-6 col-md-4 col-lg-1 text-center">
              
              <music :details="music" />
              <!-- <music :details="music" /> -->
          </div>
      </div>
      <!-- <Loader v-else ladel="Vue-dischi" /> -->
      <!-- <Song /> -->
  </section>
</template>

<script>
import axios from 'axios';
import music from '@/components/music.vue'
// import Loader from '@/components/Loader.vue';
// import Song from '@/components/Song.vue';


export default {
    name: 'Album',
    components: {
        music
        // Song,
        // Loader
    },
    data() {
        return {
            apiURL : 'https://flynn.boolean.careers/exercises/api/array/music',
            Album : '',
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
                .then(res => {
                    if (res.data.success == true){
                        console.log(res.data.response);
                        this.Album = res.data.response;
                        console.log(this.Album);
                        this.loading = false;
                    }
                    
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