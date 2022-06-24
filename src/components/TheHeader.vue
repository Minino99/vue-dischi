<template>
  <div>
    <div
      class="container-fluid px-4 py-3 d-flex justify-content-between align-items-center"
    >
      <div class="h-100">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png"
          alt="logo_spotify"
          srcset=""
        />
      </div>
      <div class="d-flex gap-4">
        <select class="form-select" v-model="selectedGenre">
          <option value="rock">Rock</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
          <option value="metal">Metal</option>
        </select>
        <button type="button" class="btn btn-outline-success" @click="$emit('selectedGenre')">Filtra per genere</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheHeader",
  components: {},
  data: function () {
    return {
      selectedGenre: "",
    };
  },
};
</script>

<style scoped lang="scss">
.container-fluid {
  height: 10vh;
  min-height: 65px;
  background-color: #2e3a46;

  img {
    height: 100%;
  }

  button{
   white-space: nowrap;
  }
}
</style>
