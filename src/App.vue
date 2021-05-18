<template>
  <div id="app">
    <Navbar />
    <ScociaBar />
    <vue-page-transition name="fade">
      <router-view />
    </vue-page-transition>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import ScociaBar from "@/components/StickySocialBar.vue";

export default {
  components: {
    Navbar,
    ScociaBar,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Balsamiq+Sans&family=Eczar:wght@600&display=swap");
#app {
  font-family: Eczar, Balsamiq Sans, Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  background-color: black;
}
</style>
