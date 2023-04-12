<template>
  <div class="mx-auto pt-[10px] relative text-light-black max-w-[1280px]">
    <Header />
    <div class="flex gap-5">
      <Profile />
      <Information />
    </div>
    <Footer />
  </div>
</template>
<script setup lang="ts">
import Header from './components/Header.vue';
import Footer from './components/Footer.vue'
import Profile from './components/Profile.vue';
import Information from './components/Information.vue';
</script>
<style scoped>
body {
  background: #fafafd;
}
html {
  scroll-behavior: smooth;
}
</style>
