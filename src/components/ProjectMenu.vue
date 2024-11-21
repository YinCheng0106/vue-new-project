<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faLink } from '@fortawesome/free-solid-svg-icons';
import { ref } from 'vue';
let id = 0;
const project_list = ref([
    {id: id++, name: "YINLA", img: "/favicon.ico", link: "https://github.com/YINLA-TEAM/YINLA", desc: "這是一隻Discord的BOT，不定時會更新 主要功能是檢視天氣、檢視地震(含推播功能)、文字翻譯、查詢中油油價(含推播功能)以及查詢中華職棒相關的功能"},
    {id: id++, name: "discord-bot-rpg", img: "", link: "https://github.com/YINLA-TEAM/discord-bot-rpg", desc: "開發中..."},
]);

</script>

<template>
    <div>
        <h3>PROJECT</h3>
    </div>
    <div>
        <ul>
            <li v-for="project in project_list" :key="project.id">
                <img class="project_img" src=/favicon.ico>
                <h3>{{ project.name }}</h3>
                <p>{{ project.desc }}</p>
                <a href="https://github.com/YINLA-TEAM/YINLA"><FontAwesomeIcon :icon="faLink" /> GitHub</a>
            </li>
        </ul>
    </div>
</template>

<style scoped>
    h3 {
        font-family: monospace;
        font-size: 1.2rem;
    }

    .project_img {
        height: 64px;
        float: right;
        border-radius: 12px;
    }

    li {
        border-radius: 12px;
        padding: 12px;
        list-style-type: none
    }

    @media (hover: hover) {
        li:hover {
            background-color: rgb(255, 255, 255, 0.2);
        }
    }
</style>