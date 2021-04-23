<template>
  <div id="app-wrapper">
    <Infobar />
    <Searchbar />
    <Navbar />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Infobar from "./components/Infobar.vue";
import Searchbar from "./components/Searchbar.vue";
import Navbar from "./components/Navbar/Navbar.vue";

export default defineComponent({
  name: "App",
  components: {
    Infobar,
    Searchbar,
    Navbar,
  },
});
</script>

<style></style>
