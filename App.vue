<script setup>
import { ref } from 'vue';
import WebTitle from './components/WebTitle.vue';
import ProjectMenu from './components/ProjectMenu.vue';
let id = 0;
const nav_link = ref([
  { id: id++, text: "GitHub", link: "https://github.com/YINLA-TEAM" },
  { id: id++, text: "Discord", link: "https://discord.gg/mnCHdBbh65" }
]);
</script>

<template>
  <nav>
    <ul>
      <li v-for="nav in nav_link" :key="nav.id">
        <a :href=nav.link target="_blank">{{ nav.text }}</a>
      </li>
    </ul>
  </nav>

  <header>
    <div class="wrapper">
      <a href="https://github.com/YINLA-TEAM"><img class="logo" src="/favicon.ico" alt="YINLA_v2"></a>
      <WebTitle title="YINLA" />
      <img class="skills" src="https://skillicons.dev/icons?i=html,css,js,py,md,vue,vite,docker,discordjs" alt="Skills : html,css,js,py,md,vue,vite,docker,discordjs">
    </div>
  </header>

  <main>
    <ProjectMenu />
  </main>

  <footer class="footer">
    Copyright © 2024 YINLA. All rights reserved.
  </footer>
</template>

<style scoped>
nav {
  margin: 0;
  padding: 0;
}

ul,li {
  display: flex;
  gap: 12px;
  border-radius: 12px;
  padding: 12px;
  list-style-type: none;
}

header {
  line-height: 1.5;
}

.logo {
  height: 64px;
  display: flex;
  margin: 0 auto;
  border-radius: 24px;
}

.skills {
  display: block;
  margin: 0 auto;
}

.footer {
  text-align: center;
  margin-top: auto;
  padding: 1rem 0;
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
