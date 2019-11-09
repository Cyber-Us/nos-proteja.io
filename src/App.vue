<template>
  <div id="app">
    <Search></Search>
  </div>
</template>

<script>
import Search from "./components/Search.vue";

export default {
  name: "app",
  components: {
    Search
  }
};
</script>

<style>
html {
  background-color: #2c353a;
  overflow-y: scroll;
  font-family: Open Sans, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  -webkit-font-smoothing: antialiased;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
body {
  margin: 0;
  padding: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
