<script setup>
import { ref } from "vue";
const links = ref([
  {
    id: 1,
    text: "About Me",
    url: "/about",
  },
  {
    id: 2,
    text: "Projects",
    url: "/projects",
  },
  {
    id: 3,
    text: "Contact",
    url: "/contact",
  },
]);
</script>
<template>
  <div class="fixed h-screen flex flex-col-reverse justify-center gap-14 p-5">
    <div class="text-vertical" v-for="link in links" :key="link.id">
      <a :href="link.url">{{ link.text }}</a>
    </div>
  </div>
</template>
<style>
.text-vertical {
  writing-mode: vertical-lr;
  transform: rotate(180deg);
}
.text-vertical a {
  text-transform: uppercase;
}
</style>
