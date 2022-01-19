<template>
  <section
    class="mountain relative flex justify-center items-center w-full h-screen overflow-hidden"
  >
    <img src="@/assets/img/stars.png" alt="" id="stars" />
    <img
      src="@/assets/img/moon.png"
      alt=""
      id="moon"
      class="mix-blend-screen"
    />
    <img src="@/assets/img/mountains_behind.png" alt="" id="mountains" />
    <h2 id="text" class="absolute text-white font-semibold text-9xl">
      Moon Light
    </h2>
    <a href="#" class="btn">Explore</a>
    <img src="@/assets/img/mountains_front.png" />
  </section>
</template>

<script>
export default {
  name: "mountain",
  created() {},
};

window.addEventListener("scroll", function () {
  let value = window.scrollY;

  document.getElementById("stars").style.left = value * 0.25 + "px";
  document.getElementById("moon").style.top = value * 1.05 + "px";
  document.getElementById("mountains").style.top = value * 0.5 + "px";
});
</script>

<style lang="scss" scoped>
.mountain {
  img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    pointer-events: none;
  }
  .btn {
    text-decoration: none;
    padding: 8px 30px;
    border-radius: 40px;
    background: #fff;
    color: #2b1055;
    font-size: 1rem;
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
