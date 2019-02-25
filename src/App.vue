<template>
  <div id="app">
    <Main></Main>
    <router-view></router-view>
  </div>
</template>

<script>
import Main from "./components/Main";
export default {
  name: "app",
  components: {
    Main
  }
};
</script>

<style>
html {
  background: #ffffff; /* Old browsers */
  background: -moz-linear-gradient(
    top,
    #ffffff 0%,
    #e5e5e5 100%
  ); /* FF3.6-15 */
  background: -webkit-linear-gradient(
    top,
    #ffffff 0%,
    #e5e5e5 100%
  ); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(
    to bottom,
    #ffffff 0%,
    #e5e5e5 100%
  ); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#e5e5e5',GradientType=0 ); /* IE6-9  */
  background-repeat: no-repeat;
}

body {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
}

ul {
  list-style: none;
}

ul,
li {
  margin: 0;
  padding: 0;
}

#app {
  font-family: "Open Sans", Helvetica, Arial, sans-serif;
  background-color: #000000;
}
</style>
