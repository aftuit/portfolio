<template>
  <div class="wrapper d-flex">
    <Navbar :nav="nav" :openSidebar="openSidebar"/>
    <div class="shadow" :class="nav? ' show': ''"></div>
    <div class="right-side h-100 w-100 bg-dark text-white">

      <div class="burger ms-5 mt-5 d-none" @click="openSidebar">
        <i class="fa-solid fa-bars fa-2xl" style="color: rgb(255 255 255 / 70%);"></i>
      </div>
      <RouterView />
    </div>
  </div>
</template>
<script>
import { Navbar } from "./components";
import { RouterView } from "vue-router";
// import RouterVue from "vue-router"
export default {
  components: {
    Navbar
  },
  data() {
    return {
      nav: false,
      show: false,
      screen: screen.width,
    }
  },

  methods: {
    openSidebar() {
      this.nav = !this.nav;
    }
  },
  
};
</script>
<style>
</style>