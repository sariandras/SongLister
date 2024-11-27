
<template>
  <div class="container">
    <h1>Songs</h1>
    <br>
    <SelectArtist :artists="artistData" @change-artist="filterSongs($event)"/>
    <SongList v-if="songs.length!=0" :songs="songs"/>
  </div>
</template>

<script setup>
import artistData from './artists';
import SelectArtist from './components/selectArtist.vue';
import SongList from './components/songList.vue';
import songsData from './songs';
import { ref } from 'vue';

const songs = ref([]);

// const changeArtist = (artistId)=>{
//   songs.value = songsData.filter(s=>s.ARTIST_ID==artistId);
// }
const filterSongs = (id)=>{
  songs.value = songsData.filter(s=>s.ARTIST_ID==id);

}
</script>
<style scoped>

</style>
