<template>
  <div id="app">
    <main-page></main-page>
  </div>
</template>

<script>
import MainPage from "./components/MainPage.vue";

export default {
  name: "app",
  components: {
    MainPage
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
  margin-top: 60px;
}
</style>