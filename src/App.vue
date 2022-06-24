<template>
<div id="app">
  <TheHeader :fetchGenre="genreInput"/>
  <AlbumCards/>
</div>
</template>

<script>
import TheHeader from './components/TheHeader.vue'
import AlbumCards from './components/AlbumCards.vue'
export default {
  name: 'App',
  components: {TheHeader, AlbumCards},
  methods: {
    genreInput(genre) {
      console.log(genre)
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
