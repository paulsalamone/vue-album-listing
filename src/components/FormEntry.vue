<script setup>
import { ref, reactive } from "vue";

// const newAlbum = reactive({
//   artist: "x",
//   title: "y",
//   genre: "z",
//   year: 0,
// });

const albums = ref([
  {
    artist: "Pavement",
    title: "Slanted and Enchanted",
    genre: "indie rock",
    year: 1992,
    cover: 0,
  },
  {
    artist: "Pavement",
    title: "Slanted and Enchanted",
    genre: "indie rock",
    year: 1992,
    cover: 0,
  },
  {
    artist: "Pavement",
    title: "Slanted and Enchanted",
    genre: "indie rock",
    year: 1992,
    cover: 0,
  },
]);

const artist = ref("");
const title = ref("");
const genre = ref("");
const year = ref(1999);

const show = ref(true);
function toggleShow() {
  show.value = !show.value;
}
</script>

<template>
  <h2>Create New Album: <button @click="toggleShow">hide</button></h2>
  <br />
  <form v-if="show">
    <input v-model="artist" placeholder="artist" />
    <input v-model="title" placeholder="title" />
    <input v-model="genre" placeholder="genre" />
    <input v-model="year" placeholder="year" />
    <button type="submit">submit</button>
  </form>
  <div class="album-listing">
    <div :key="index" v-for="(album, index) in albums">
      <div class="album-cover">
        <h3>{{ album.artist }}</h3>
        <h2>{{ album.title }}</h2>
        <h4>{{ album.genre }}, {{ album.year }}</h4>
      </div>
    </div>
  </div>
</template>

<style>
form {
  background-color: #ffaacc;
  padding: 10px;
  display: flex;
  flex-direction: column;
}
input {
  margin: 5px;
  padding: 5px 7px;
}
button {
  background-color: black;
  color: white;
  border: 0px;
  padding: 7px 10px;
  border-radius: 5px;
}
.album-listing {
  display: grid;
  grid-template-columns: 1fr 1fr;
}
.album-cover {
  background-color: grey;
  margin: 5px;
  color: white;
  padding: 10px;
}
</style>
