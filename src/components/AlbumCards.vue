<template>
  <div>
    <div class="container">
      <div class="row align-items-center justify-content-center gap-5">
        <div
          v-for="album in Albums"
          :key="album.title"
          class="col-2 albumcontainer"
        >
          <div class="albumimg py-4">
            <img :src="album.poster" alt="" class="w-100" />
          </div>
          <h5 class="pb-2 text-center albumtitle">
            {{ album.title.toUpperCase() }}
          </h5>
          <div class="text-center albumsubtitle">{{ album.author }}</div>
          <div class="pb-5 text-center albumsubtitle">{{ album.year }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "AlbumCards",
  components: {},
  data() {
    return {
      Albums: [],
    };
  },
  methods: {
    fetchDisks() {
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((response) => {
          this.Albums = response.data.response;
          console.log(this.Albums);
        });
    },
  },
  mounted() {
    this.fetchDisks();
  },
};
</script>

<style scoped lang="scss">
.container {
  height: 90vh;
  overflow: auto;
  transform: scale(0.8);
}

.albumcontainer {
  background-color: #2e3a46;
  height: 400px;
}

.albumtitle {
  color: white;
  font-weight: 700;
}

.albumsubtitle {
  color: gray;
}
</style>
