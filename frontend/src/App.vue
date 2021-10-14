<template>
  <div id="app">
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from "./components/layouts/Navbar.vue";
export default {
  components: {
    Navbar,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Kanit:wght@300&display=swap");
* {
  font-family: "Kanit", sans-serif;
}
</style>