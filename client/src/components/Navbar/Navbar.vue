<template>
  <div id="navbar">
    <Category
      @mouseenter="hoverCategory"
      @mouseleave="leaveCategory"
      :key="i"
      v-for="i in categoryList.length"
      :category="categoryList[i - 1]"
    />
  </div>
</template>

<script lang="ts">
// NOTE ABOVE THAT THE REASON FOR categoryList[i - 1] IS THAT
// v-for IS 1-INDEXED INSTEAD OF 0-INDEXED
import { defineComponent } from "vue";
import Category from "./Category.vue";

export default defineComponent({
  name: "Navbar",
  components: {
    Category,
  },
  data() {
    return {
      categoryList: [
        "CATEGORY 1",
        "CATEGORY 2",
        "CATEGORY 3",
        "CATEGORY 4",
        "CATEGORY 5",
        "CATEGORY 6",
      ],
    };
  },
  methods: {
    // hoverCategory and leaveCategory are two mouseover event listeners
    // that accomplish the same thing a CSS parent selector could have.
    // When hovering on a div, change all sibling divs to a different text color.
    hoverCategory(event: any) {
      const allCategories = document.querySelectorAll<HTMLElement>(".category");
      const targetedCategory: HTMLElement = event.target;
      allCategories.forEach((category) => {
        if (category !== targetedCategory) {
          category.style.color = "rgb(190, 190, 190)";
        }
      });
    },
    leaveCategory() {
      const allCategories = document.querySelectorAll<HTMLElement>(".category");
      allCategories.forEach((category) => (category.style.color = "#454545"));
    },
  },
});
</script>

<style>
#navbar {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  width: 80%;
  margin: 2em auto;
}
@media (max-width: 900px) {
  #navbar {
    display: none;
  }
}
</style>
