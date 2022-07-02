<script setup>
import { ref, computed } from "vue";
import Layout from "../components/Layout.vue";

const domain = ['Aamir','your RDMS','full stack developer', 'your bot developer']
function sleep(ms) {
      return new Promise(resolve => setTimeout(resolve, ms));
   }
const change = computed(()=>{

    for (let x in domain) {
      sleep(10);
      return domain[x];
  }
})
  
const buttons = ref([
  {
    id: 1,
    text: "Github",
    url: "#",
  },
  {
    id: 2,
    text: "Linkedin",
    url: "#",
  },
  {
    id: 3,
    text: "Fiverr",
    url: "#",
  },
]);
</script>

<template>
  <Layout>
    <div class="flex flex-col">
      <h1 class="text-9xl font-bold text-[#5B5151]">Hi,</h1>
      <h1 class="text-9xl text-[#5B5151]">
        I am <span class="underline"> {{ change }}</span>
      </h1>
      <div class="flex flex-row gap-6 my-7">
        <a v-for="button in buttons" :key="button.id" :href="button.url"
          ><button class="py-3 px-2 border-2 border-[#557B83] text-[#557B83]">
            {{ button.text }}
          </button>
        </a>
      </div>
    </div>
  </Layout>
</template>
