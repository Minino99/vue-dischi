<template>
<div>
 <div class="container-fluid px-4 py-3">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="logo_spotify" srcset="">
 </div>
</div>
</template>

<script>
export default {
  name: 'TheHeader',
  components: {}
}
</script>

<style scoped lang="scss">
.container-fluid{
 height: 10vh;
 min-height: 65px;
 background-color: #2E3A46;

 img{
  height: 100%;
 }
}

</style>