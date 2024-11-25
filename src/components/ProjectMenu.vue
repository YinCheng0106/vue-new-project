<script setup>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faExternalLink } from '@fortawesome/free-solid-svg-icons';
import { ref } from 'vue';

let id = 0;
const project_list = ref([
    {id: id++, name: "YINLA", img: "/favicon.ico", link: "https://github.com/YINLA-TEAM/YINLA", desc: "這是一隻Discord的BOT，不定時會更新 主要功能是檢視天氣、檢視地震(含推播功能)、文字翻譯、查詢中油油價(含推播功能)以及查詢中華職棒相關的功能"},
    {id: id++, name: "discord-bot-rpg", img: "", link: "https://github.com/YINLA-TEAM/discord-bot-rpg", desc: "開發中..."},
    {id: id++, name: "YINLA-TEAM.github.io", img: "", link: "https://github.com/YINLA-TEAM/YINLA-TEAM.github.io", desc: "YINLA 官網"},
]);

</script>

<template>
    <div>
        <h2>PROJECT</h2>
    </div>
    <div>
        <ul>
            <li v-for="project in project_list" :key="project.id">
                <img class="project_img" :src="project.img">
                <h3>{{ project.name }}</h3>
                <p>{{ project.desc }}</p>
                <a class="project_link" :href="project.link" target="_blank">GitHub <FontAwesomeIcon :icon="faExternalLink"/></a>
            </li>
        </ul>
    </div>
</template>

<style scoped>
    h2 {
        font-weight: bold;
        font-family: monospace;
        font-size: 2rem;
    }
    
    h3 {
        font-weight: bold;
        font-family: monospace;
        font-size: 1.2rem;
    }

    .project_img {
        height: 64px;
        margin-left: 12px;
        float: right;
        border-radius: 12px;
    }

    .project_link {
        /* float: right; */
        padding: 4px;
        text-align: center;
        color: black;
        background-color: rgba(255, 255, 255, 0.5);
        border-radius: 4px;
    }

    .project_link:hover {
        background-color: rgb(255, 255, 255);
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