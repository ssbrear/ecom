<template>
  <div id="infobar">
    <h2 id="infobar-slogan">Lorem ipsum dolor</h2>
    <ul id="infobar-links">
      <li><a href="#">ABOUT US</a></li>
      <li><a href="#">CONTACT US</a></li>
      <li><a href="#">FREQUENT QUESTIONS</a></li>
    </ul>
    <h2 id="infobar-phone-number">123-456-7890</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Infobar",
});
</script>

<style scoped>
#infobar {
  display: grid;
  font-family: Poppins;
  background: #222222;
  color: #eaeaea;
}
#infobar > * {
  margin: 0;
  padding: 1.25em 1em;
  align-self: center;
}
#infobar-slogan {
  justify-self: flex-start;
  grid-column: 1/2;
  color: white;
  font-size: 1rem;
  padding: 0 1em;
}
#infobar-links {
  list-style: none;
  grid-column: 3/4;
  display: flex;
  justify-self: end;
  font-size: 0.8125rem;
}
#infobar-links > li {
  margin: 0 1em;
}
a:hover {
  opacity: 0.75;
  transition: 0.3s;
}
#infobar-phone-number {
  width: 100%;
  text-align: center;
  grid-column: 4/5;
  justify-self: center;
  padding-left: 0;
  padding-right: 0;
  font-size: 0.8125rem;
  font-weight: 300;
  border-left: 1px solid grey;
}
@media (max-width: 900px) {
  #infobar {
    grid-template-columns: auto;
  }
  #infobar-links,
  #infobar-phone-number {
    display: none;
  }
  #infobar-slogan {
    justify-self: center;
    padding: 0.75em 0;
  }
}
</style>
