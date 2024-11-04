<script setup>
import { ref } from "vue";
import cssImg from "@/assets/img/skills/css.png";
import dockerImg from "@/assets/img/skills/docker.png";
import expressImg from "@/assets/img/skills/express.png";
import githubImg from "@/assets/img/skills/github.png";
import gitlabImg from "@/assets/img/skills/gitlab.png";
import htmlImg from "@/assets/img/skills/html.png";
import javascriptImg from "@/assets/img/skills/javascript.png";
import laravelImg from "@/assets/img/skills/laravel.png";
import mongodbImg from "@/assets/img/skills/mongodb.png";
import mysqlImg from "@/assets/img/skills/mysql.png";
import nodejsImg from "@/assets/img/skills/nodejs.png";
import nuxtImg from "@/assets/img/skills/nuxt.png";
import phpImg from "@/assets/img/skills/php.png";
import postgreeImg from "@/assets/img/skills/postgree.png";
import tailwindImg from "@/assets/img/skills/tailwind.png";
import typescriptImg from "@/assets/img/skills/typescript.png";
import vueImg from "@/assets/img/skills/vue.png";

const skills = ref([
  {
    categories: "Technology & Basic",
    items: [
      { name: "Php", image: phpImg },
      { name: "Javascript", image: javascriptImg },
      { name: "Node JS", image: nodejsImg },
      { name: "Typescript", image: typescriptImg },
      { name: "HTML5", image: htmlImg },
      { name: "CSS3", image: cssImg },
    ],
  },
  {
    categories: "Framework",
    items: [
      { name: "Express JS", image: expressImg },
      { name: "Laravel", image: laravelImg },
      { name: "Vue JS", image: vueImg },
      { name: "Nuxt JS", image: nuxtImg },
      { name: "Tailwind CSS", image: tailwindImg },
    ],
  },
  {
    categories: "Database & Infrastructure",
    items: [
      { name: "MySQL", image: mysqlImg },
      { name: "PostgreSQL", image: postgreeImg },
      { name: "MonggoDB", image: mongodbImg },
      { name: "Github", image: githubImg },
      { name: "Gitlab", image: gitlabImg },
      { name: "Docker", image: dockerImg },
    ],
  },
]);
</script>

<template>
  <div v-for="(data, i) in skills" class="w-full box-border mt-10">
    <h1 class="font-semibold my-10 font-semibold text-xl lg:text-lg text-white">{{ data.categories }}:</h1>
    <div class="w-full grid grid-cols-4 lg:grid-cols-5 gap-x-4 gap-y-8">
      <div class="w-full flex flex-col items-center justify-center" v-for="(item, i) in data.items">
        <img :src="item.image" alt="" class="h-12 lg:h-24 mb-2" />
        <h5 class="text-sm lg:text-base">{{ item.name }}</h5>
      </div>
    </div>
  </div>
</template>
