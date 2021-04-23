<template>
  <a href="#" class="category">{{ category }}</a>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Category",
  props: {
    category: String,
  },
});
</script>

<style scoped>
.category {
  font-family: Poppins, Arial, Helvetica, sans-serif;
  font-size: 0.875rem;
  font-weight: 600;
  margin: auto;
  transition: color 0.2s ease-in-out;
  color: #454545;
}
</style>
