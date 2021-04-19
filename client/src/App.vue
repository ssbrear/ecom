<template>
  <div id="app-wrapper">
    <Navbar />
    <Searchbar />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Navbar from "./components/Navbar.vue";
import Searchbar from "./components/Searchbar.vue";

export default defineComponent({
  name: "App",
  components: {
    Navbar,
    Searchbar,
  },
});
</script>

<style></style>
