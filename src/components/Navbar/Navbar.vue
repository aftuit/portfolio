<template>
  <div
    class="d-flex flex-column flex-shrink-0 p-3 text-white bg-dark-50 h-100 justify-content-center sidebar"
    :class="nav? ' show': ''"
  >
  <div class="text-center sidebar-content">
      <i @click="openSidebar" class="fa-solid fa-xmark fa-2xl close" style="color: rgba(255,255,255,0.7);"></i>
      <h1
        class="text-white mb-3"
      >
        <span class="fs-4">Aktamovs Dev</span>
      </h1>
      <hr />
      <ul class="nav nav-pills flex-column mb-auto mt-5">
        <li class="nav-item">
          <RouterLink :to="{name: 'home'}" class="nav-link text-light"
          @click="changeLink"
          > Home </RouterLink>
        </li>
        <li class="nav-item">
          <RouterLink :to="{name: 'about'}" class="nav-link text-light"
          @click="changeLink"
          > About </RouterLink>
        </li>
        <li class="nav-item">
          <RouterLink :to="{name: 'portfolio'}" class="nav-link text-light"
          @click="changeLink"
          >
            Portfolio
          </RouterLink>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
import "./style.css"
import { logo } from "../../const";
import { RouterLink } from "vue-router";
export default {
  props: {
    nav: {
      type: Boolean,
      required: true
    },
    openSidebar: {
      type: Function,
      required: true
    }
  },
  data() {
    return {
      logo,
      activeLink: '1',
    };
    
  },
  methods :{
    changeLink() {
      this.openSidebar();
    }
  }
};
</script>
<style scoped>


</style>