<template>
  <div>
    <div
      class="absolute z-50 w-full flex justify-between items-center py-10 px-24"
    >
      <a href="#">
        <span class="sr-only">Logo</span>
        <h1 class="text-white text-3xl font-bold uppercase">Logo</h1>
      </a>

      <nav>
        <ul>
          <li
            v-for="(item, index) in listNavbar"
            :key="index"
            class="nav-item inline-block text-white relative w-20"
          >
            <a :href="item.link" @click="setActive(index)">{{ item.title }}</a>
            <hr
              v-if="index == 0"
              class="active absolute bg-white left-0 rounded h-1 w-10 duration-150"
              id="active"
            />
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  components: {},
  data() {
    return {
      active: "Home",
      listNavbar: [
        {
          title: "Home",
          link: "#home",
        },
        {
          title: "Pricing",
          link: "#pricing",
        },
        {
          title: "About",
          link: "#about",
        },
        {
          title: "Contact",
          link: "#contact",
        },
      ],
    };
  },
  methods: {
    setActive(index) {
      document.getElementById("active").style.left = 5 * index + "rem";
    },
  },
};
</script>
