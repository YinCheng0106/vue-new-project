<script setup>
import WebTitle from './components/WebTitle.vue';
import ProjectMenu from './components/ProjectMenu.vue';
</script>

<template>
  <header>
    <div class="wrapper">
      <a href="https://github.com/YINLA-TEAM"><img class="logo" src="/favicon.ico" alt="YINLA_v2"></a>
      <WebTitle title="YINLA" />
    </div>
  </header>

  <main>
    <ProjectMenu />
  </main>
  <footer>
    Copyright © 2024 YINLA. All rights reserved.
  </footer>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  height: 64px;
  display: block;
  margin: 0 auto 2rem;
  border-radius: 24px;
}

footer {
  text-align: center;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
