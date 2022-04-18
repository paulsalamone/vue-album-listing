<script setup>
import { ref } from "vue";

const hide = ref(true);

function hideToggled() {
  hide.value = !hide.value;
}
</script>

<template>
  <button @click="hideToggled">Description:</button>

  <p v-if="hide">
    This is a mini-project to practice Vue. I want to have a form where the user
    can add an album with the fields Artist, Album, Genre, and Year. Albums are
    listed, then they call sort the view based on any of the categories. Each
    one also has a randomly-generated cover image. BONUS: filter results with
    search input. Use p5 for images.
  </p>
</template>
