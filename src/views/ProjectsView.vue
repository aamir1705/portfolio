<script setup>
import { ref } from "vue";
import Layout from "../components/Layout.vue";
import Handling from "../components/TextHand.vue";
import ui from '../assets/ui&ux.png'
import frontend from '../assets/frontend.png'
import python from '../assets/python.jpeg'
const images = ref([
  {
    id: 1,
    url: "/ui&ux",
    image: ui,
  },
  {
    id: 2,
    url: "/frontend",
    image: frontend,
  },
  {
    id: 3,
    url: "/backend",
    image: python,
  },
  {
    id: 4,
    url: "/python",
    image: python,
  },
]);
</script>
<template>
  <Layout>
    <Handling text="Projects" />
    <div class="flex flex-col gap-4 h-36">
      <a v-for="image in images" :key="image.id" :href="image.url">
        <img  :src="image.image" alt="" />
      </a>
    </div>
  </Layout>
</template>
