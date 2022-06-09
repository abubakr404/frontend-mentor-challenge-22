<script setup>
import HeaderPage from "./components/HeaderPage.vue";
import MainBlogr from "./components/MainBlogr.vue";
import FooterPage from "./components/FooterPage.vue";
</script>

<template>
  <header>
    <HeaderPage />
  </header>

  <main>
    <MainBlogr />
  </main>

  <footer>
    <FooterPage />
  </footer>
</template>

<style>
@import "./assets/css/main.css";
div#app {
  overflow-x: hidden;
}
</style>
