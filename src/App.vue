<!-- src/App.vue -->
<template>
  <div id="app">
    <Nav />
    <router-view />
  </div>
</template>

<script>
import Nav from "./components/NavList.vue";

export default {
  name: "App",
  components: {
    Nav,
  },
};
</script>

<style>
/* 你可以在这里添加全局样式 */
</style>
