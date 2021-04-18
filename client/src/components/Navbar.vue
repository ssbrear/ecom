<template>
  <div id="navbar">
    <h2 id="navbar-slogan">Lorem ipsum dolor</h2>
    <ul id="navbar-links">
      <li><a href="#">ABOUT US</a></li>
      <li><a href="#">CONTACT US</a></li>
      <li><a href="#">FREQUENT QUESTIONS</a></li>
    </ul>
    <h2 id="navbar-phone-number">123-456-7890</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Navbar",
  props: {
    msg: String,
  },
});
</script>

<style scoped>
#navbar {
  display: grid;
  font-family: "Poppins";
  background: #222222;
  color: #eaeaea;
  grid-template-columns: 2fr 3fr 3fr 1fr;
}
#navbar > * {
  margin: 0;
  padding: 0.75em 1em;
  align-self: center;
}
#navbar-slogan {
  justify-self: flex-start;
  grid-column: 1/2;
  color: white;
  font-size: 1rem;
}
#navbar-links {
  list-style: none;
  grid-column: 3/4;
  display: flex;
  justify-self: center;
  font-size: 0.8125rem;
}
#navbar-links > li {
  margin: 0 1em;
}
a:hover {
  opacity: 0.75;
  transition: 0.3s;
}
#navbar-phone-number {
  width: 100%;
  text-align: center;
  grid-column: 4/5;
  font-size: 0.8125rem;
  font-weight: 300;
  border-left: 1px solid grey;
}
@media (max-width: 1200px) {
  #navbar {
    grid-template-columns: 2fr 2fr 4fr 1fr;
  }
}
@media (max-width: 900px) {
  #navbar {
    grid-template-columns: auto;
  }
  #navbar-links,
  #navbar-phone-number {
    display: none;
  }
  #navbar-slogan {
    justify-self: center;
  }
}
</style>
