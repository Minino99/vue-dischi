<template>
<div id="app">
  <TheHeader v-on:fetchGenre="genreInput"/>
  <AlbumCards :filtergenre="selectedGenre"/>
</div>
</template>

<script>
import TheHeader from './TheHeader.vue'
import AlbumCards from './AlbumCards.vue'
export default {
  name: 'WholeApp',
  components: {TheHeader, AlbumCards},
  data: function () {
    return {
      selectedGenre: '',
    };
  },
  methods: {
    genreInput(genre) {
      this.selectedGenre = genre
    }
  },
}
</script>

<style lang="scss">

#app{
  height: 100vh;
  background-color: #1E2D3B;
  }
</style>
