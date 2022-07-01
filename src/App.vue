<template>
  <SegwNavbar />
  <router-view />
</template>

<script>
import SegwNavbar from "./components/SegwNavbar.vue";

export default {
  name: "App",
  components: {
    SegwNavbar
  }
};
</script>

<style>
nav a.router-link-exact-active {
  color: #f06608;
}
</style>
