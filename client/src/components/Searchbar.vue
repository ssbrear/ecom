<template>
  <div id="searchbar">
    <button id="searchbar-menu"><i class="fas fa-bars fa-2x"></i></button>
    <img id="searchbar-logo" src="https://via.placeholder.com/117x65" />
    <div id="searchbar-input-div">
      <input placeholder="Search" id="searchbar-input" />
      <button id="searchbar-search-button">
        <i class="fas fa-search"></i>
      </button>
    </div>
    <button id="searchbar-login"><i class="fas fa-user"></i>SIGN IN</button>
    <button id="searchbar-cart">
      <i class="fas fa-shopping-cart"></i>CART
    </button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "Searchbar",
});
</script>

<style scoped>
#searchbar {
  display: grid;
  font-family: Poppins;
  padding: 0.75em;
  grid-auto-flow: column;
  border-bottom: 1px solid rgb(219, 219, 219);
}
#searchbar-menu {
  display: none;
}
#searchbar-logo {
  grid-column: 1/2;
}
button {
  border: none;
  cursor: pointer;
  outline: none;
  background: none;
}
#searchbar-input-div {
  grid-column: 5/6;
  align-self: center;
  justify-self: end;
  position: relative;
}
#searchbar-input {
  height: 2em;
  padding: 0.5em 2em;
  border: 1px solid rgb(230, 230, 230);
  width: 30em;
}
#searchbar-search-button {
  grid-column: 5/6;
  z-index: 1;
  position: relative;
  right: 40px;
  bottom: 3px;
  padding: 20px;
}
#searchbar-search-button > i {
  position: absolute;
  right: 15px;
  bottom: 13px;
}
#searchbar-login {
  font-size: 1rem;
  font-family: inherit;
  grid-column: 6/7;
  justify-self: end;
  align-self: center;
  padding-right: 1.25em;
}
#searchbar-login > i {
  position: relative;
  right: 10px;
}
#searchbar-cart {
  font-size: 1rem;
  font-family: inherit;
  grid-column: 7/8;
  justify-self: start;
  align-self: center;
  padding-left: 1.3125em;
  border-left: 1px solid rgb(201, 201, 201);
}
#searchbar-cart > i {
  position: relative;
  right: 10px;
}
@media (max-width: 900px) {
  #searchbar-login {
    display: none;
  }
  #searchbar-cart {
    grid-column: 5/6;
    grid-row: 1/2;
    border: none;
    justify-self: end;
    position: relative;
    right: 15px;
  }
  #searchbar {
    grid-auto-flow: row;
    justify-items: center;
    align-items: center;
  }
  #searchbar-logo {
    grid-column: 3/4;
    grid-row: 1/2;
  }
  #searchbar-input-div {
    grid-column: 1/6;
    grid-row: 2/3;
    width: 100%;
  }
  #searchbar-input {
    width: calc(100% - 5em);
  }
  #searchbar-search-button {
    position: absolute;
    right: 12px;
    top: 1px;
  }
  #searchbar-menu {
    display: inline-block;
    grid-column: 1/2;
    grid-row: 1/2;
    justify-self: start;
    position: relative;
    left: 15px;
  }
}
</style>
