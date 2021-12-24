<template>
  <div id="app">
    <navbar></navbar>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
    Navbar: () => import("@/components/Navbar.vue"),
  },
};
</script>

<style lang="scss">
@import "@/assets/css/app.scss";
</style>
