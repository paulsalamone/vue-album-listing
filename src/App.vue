<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import TheWelcome from "./components/TheWelcome.vue";
import ProjDescription from "./components/ProjDescription.vue";
import FormEntry from "./components/FormEntry.vue";
import AlbumList from "./components/AlbumList.vue";
</script>

<template>
  <header>
    <h1>Album List Builder</h1>
    <ProjDescription />
  </header>

  <main>
    <FormEntry />
    <AlbumList />
  </main>
</template>

<style>
header {
  background-color: #efff33;
  padding: 10px;
}
</style>
