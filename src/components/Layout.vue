<script setup>
import Navbar from "./Navbar.vue";
</script>

<template>
  <div class="flex">
    <Navbar></Navbar>
    <slot></slot>
  </div>
</template>
