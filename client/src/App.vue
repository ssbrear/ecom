<template>
  <div id="app-wrapper">
    <Infobar />
    <Searchbar />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Infobar from "./components/Infobar.vue";
import Searchbar from "./components/Searchbar.vue";

export default defineComponent({
  name: "App",
  components: {
    Infobar,
    Searchbar,
  },
});
</script>

<style></style>
