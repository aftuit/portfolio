<template >
  <div class="title">
    <span class="badge text-white-50">{{ badge }}</span>
    <h2 class="text">{{ text }}</h2>
  </div>
</template>
<script>
import "./style.css";
export default {
  props: {
    badge: {
      type: String,
      required: true,
    },
    text: {
      type: String,
      required: true,
    },
  },
};
</script>
<style >
</style>