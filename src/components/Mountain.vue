<template>
  <section class="mountain">
    <img src="@/assets/img/stars.png" alt="" id="stars" />
    <img src="@/assets/img/moon.png" alt="" id="moon" />
    <img src="@/assets/img/mountains_behind.png" alt="" id="mountains_behind" />
    <h2 id="text">Moon Light</h2>
    <a href="#" class="btn">Explore</a>
    <img src="@/assets/img/mountains_front.png" alt="" id="mountains_front" />
  </section>
</template>

<script>
export default {
  name: "mountain",
};
</script>

<style lang="scss" scoped>
.mountain {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
  padding: 100px;

  img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    pointer-events: none;
  }
  #moon {
    mix-blend-mode: screen;
  }
  #text {
    position: absolute;
    color: #fff;
    white-space: nowrap;
    font-size: 7vw;
  }
  .btn {
    text-decoration: none;
    padding: 8px 30px;
    border-radius: 40px;
    background: #fff;
    color: #2b1055;
    font-size: 1.5em;
    z-index: 9999;
    transform: translateY(100px);
  }

  &::before {
    content: "";
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100px;
    background: linear-gradient(to top, #1c0522, transparent);
    z-index: 999;
  }
}
</style>
