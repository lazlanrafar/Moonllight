<template>
  <div id="app">
    <navbar></navbar>
    <Mountain />
    <About />
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
    Navbar: () => import("@/components/Navbar.vue"),
    Mountain: () => import("@/components/Mountain.vue"),
    About: () => import("@/components/About.vue"),
  },
};
</script>

<style lang="scss">
@import "@/assets/css/app.scss";
</style>
