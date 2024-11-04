<script setup>
import { ref } from "vue";
import Navbar from "@/components/navbar/navbar.vue";
import landingImage from "@/assets/img/foto-landing.png";
import fotoFormal from "@/assets/img/foto-formal.jpg";

import InstaIcon from "@/components/icons/instagram.vue";
import TwiterIcon from "@/components/icons/twiter.vue";
import LinkedIcon from "@/components/icons/linkedin.vue";
import WorkIcon from "@/components/icons/work.vue";
import EduIcon from "@/components/icons/education.vue";

import Skills from "./Skills.vue";
import Projects from "./Projects.vue";

const workExperience = ref([
  {
    companyName: "PT. Positif Media Citra Bojonegoro",
    position: "Sr. Full Stack developer",
    date: "Jan, 2019 - Des, 2023",
    jobdesk: [
      { no: 1, content: "Optimized web application performance through code refactoring and opitimization." },
      { no: 2, content: "Implemented a microservices architecture that improved system modularity and reduced dependencies between components." },
      { no: 3, content: "Developed a sophisticated web application from scratch using the latest technologies, resulting improvement in user engagement." },
      { no: 4, content: "Implemented automated testing that increased code coverage to 90%l reducing the number of production issues." },
      { no: 5, content: "Integrated third-party services into the application to increase functionality." },
      { no: 5, content: "Developed a data warehouse that improved data access and analyst, resulting an increase in revenue." },
    ],
  },
  {
    companyName: "SMK Al Kyai Sukosewu Bojonegoro",
    position: "IT Operator",
    date: "Jun, 2017 - Ags, 2019",
    jobdesk: [
      { no: 1, content: "Managing and maintaining the school website, E-perpus, CBT, dapodik etc." },
      { no: 2, content: "Managing and maintaining the school’s network, including wired and wireless connections." },
      { no: 3, content: "Installing and configuring new hardware, software, and other tech-related tools as needed by the school." },
    ],
  },
]);

const educations = ref([
  {
    university: "Universitas Nadlatul Ulama Sunan Giri Bojonegoro",
    jurusan: "S1 - Teknik Informatika (S.Kom)",
    date: "July, 2017 - August, 2021",
  },
  {
    university: "SMAM 04 Sugihwaras",
    jurusan: "Sekolah Menengah Atas",
    date: "July, 2011 - May, 2014",
  },
  {
    university: "SMPN 02 Purwosari",
    jurusan: "Sekolah Menengah Pertama",
    date: "July, 2008 - June, 2011",
  },
]);
</script>

<template>
  <!-- 32D387 (green), 171C22 (dark), 23DB85 (light-green) -->
  <Navbar />
  <main class="conten w-screen box-border overflow-x-hidden">
    <section id="home" class="banner w-full flex lg:block flex-col relative">
      <!-- kiri -->
      <div class="mx-auto px-4 sm:px-6 lg:px-8 lg:max-w-7xl h-[600px] flex items-center">
        <div class="w-full lg:w-[600px]">
          <h5 class="text-sm font-semibold">HALLO, I'M A</h5>
          <h1 class="font-extrabold text-5xl text-white mb-5">Full Stack <span class="text-[#32D387]">Web Developer.</span></h1>
          <p class="mb-3">
            My name is M. Khoirul Huda, I'm a full-stack web developer based in Bojonegoro, Jawa Timur, Indonesia. I have developed many types of back-ends and front-ends from well know information
            system applications to Ecommerce platforms.
          </p>
          <p class="mb-5">I passionate build pixel-perfect, engaging, and accessible digital experiences.</p>
          <!-- <a href="https://drive.google.com/file/d/1LJHQLTkFeI--V73Nl1cyCYUIgO9lUQT4/view?usp=sharing" target="blank" class="bg-[#23DB85] px-4 py-3 rounded font-semibold text-white"
            >Download Resume</a
          > -->
          <a href="/M_KHOIRUL_HUDA_RESUME.pdf" target="_blank" class="bg-[#23DB85] px-4 py-3 rounded font-semibold text-white">Download Resume</a>
        </div>
      </div>

      <!-- kanan -->
      <div class="bg-[#23DB85] w-full lg:w-96 h-full relative lg:absolute lg:top-0 lg:right-0">
        <div class="lg:absolute -bottom-1 -left-52">
          <div class="w-[360px] h-[360px] lg:w-[480px] lg:h-[480px] lg:rounded-full box-border overflow-hidden relative flex items-center justify-center">
            <img :src="landingImage" alt="" class="h-full lg:h-[480px] absolute bottom-0" />
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="w-full box-border relative mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl py-10">
      <div class="w-full box-border mb-8">
        <h1 class="text-center text-3xl font-bold text-[#32D387] mb-1">About Me</h1>
        <h3 class="text-gray-500 font-semibold text-sm italic text-center">
          Here you will find additional insight about me, my skills, and a comprehensive overview of my current programming and technology skills.
        </h3>
      </div>

      <div class="w-full box-border bg-[#20272F] p-8 rounded-lg mb-10">
        <div class="flex items-start gap-x-8">
          <div class="w-24 h-24 rounded-full flex items-center justify-center flex-none border border-white bg-[#2a2838] overflow-hidden flex items-start justify-center">
            <img :src="fotoFormal" alt="" class="h-full" />
          </div>
          <div class="flex-1 w-full">
            <!-- header -->
            <div class="w-full box-border py-2 lg:py-4">
              <h1 class="text-xl lg:text-3xl font-bold mb-2 lg:mb-5">M. Khoirul Huda</h1>
              <h1 class="text-gray-500 font-semibold text-sm">Sr. Full stack developer</h1>
            </div>

            <div class="mb-8 w-full flex items-center gap-x-5">
              <a target="_blank" href="https://www.instagram.com/iroel.h" class="block text-gray-500 hover:text-gray-300">
                <InstaIcon class="size-6" />
              </a>
              <a target="_blank" href="https://x.com/irulhuda26" class="block text-gray-500 hover:text-gray-300">
                <TwiterIcon class="size-6" />
              </a>
              <a target="_blank" href="https://www.linkedin.com/in/m-khoirul-huda-32683914b" class="block text-gray-500 hover:text-gray-300">
                <LinkedIcon class="size-6" />
              </a>
            </div>
          </div>
        </div>
        <div class="flex items-start gap-x-8">
          <div class="w-24 h-24 rounded-full hidden lg:flex items-center justify-center flex-none overflow-hidden flex items-start justify-center"></div>
          <div class="flex-1 w-full">
            <p class="text-justify">
              I am a seasoned Full Stack Developer with a proven track record of over 5+ years, focusing on delivering high-quality solutions. My expertise lies in a comprehensive range of
              technologies including PHP, Laravel, JavaScript, TypeScript, Vue, Nuxt.js, Node.js, Express, Github, Docker, Kubernetes and many more. With a deep understanding of these tools and
              frameworks, I excel in crafting dynamic and scalable full-stack applications that meet the evolving needs of modern businesses. Let me bring my wealth of experience and technical prowess
              to your next project.
            </p>
          </div>
        </div>
      </div>

      <div class="w-full box-border mt-10">
        <h3 class="font-bold text-2xl text-white">Work Experience</h3>

        <div v-for="(item, i) in workExperience" class="flex gap-6 mt-6">
          <WorkIcon class="size-10" />
          <div class="w-full">
            <a target="#" class="text-xl font-semibold text-[#32D387] text-secondary-platform no-underline">
              {{ item.companyName }}
            </a>
            <div class="flex flex-col lg:flex-row justify-between items-start lg:items-center mb-4 lg:mb-2">
              <h3 class="text-lg font-medium">{{ item.position }}</h3>
              <p class="text-zinc-100 text-sm">{{ item.date }}</p>
            </div>
            <ul class="list-disc list-inside text-zinc-100 text-sm p-0">
              <li v-for="(job, i) in item.jobdesk">
                {{ job.content }}
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div class="w-full box-border mt-10">
        <h3 class="font-bold text-2xl text-white">Education</h3>

        <div v-for="(edu, i) in educations" class="flex gap-6 mt-6">
          <EduIcon class="size-10" />
          <div class="w-full">
            <a target="_blank" class="text-xl font-semibold text-[#32D387] text-secondary-platform no-underline" href="#">{{ edu.jurusan }}</a>
            <div class="flex flex-col lg:flex-row justify-between items-start lg:items-center mb-2">
              <a target="_blank" class="text-md font-normal no-underline" href="#">
                {{ edu.university }}
              </a>
              <p class="text-zinc-100 text-sm">{{ edu.date }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="skills" class="w-full box-border relative mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl py-10">
      <div class="w-full box-border mb-8">
        <h1 class="text-center text-3xl font-bold text-[#32D387] mb-1">Skills</h1>
        <!-- <h3 class="text-gray-500 font-semibold text-sm italic text-center">
          Here you will find additional insight about me, my skills, and a comprehensive overview of my current programming and technology skills.
        </h3> -->
      </div>

      <Skills />
    </section>

    <section id="projects" class="w-full box-border relative mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl py-10">
      <div class="w-full box-border mb-8">
        <h1 class="text-center text-3xl font-bold text-[#32D387] mb-1">Projects</h1>
        <!-- <h3 class="text-gray-500 font-semibold text-sm italic text-center">
          Here you will find additional insight about me, my skills, and a comprehensive overview of my current programming and technology skills.
        </h3> -->
      </div>

      <Projects />
    </section>
  </main>
  <footer class="bg-black box-border py-8">
    <p class="text-center text-sm"><span class="font-bold text-white">&copy;2024 M. Khoirul Huda</span> All Rights Reserved.</p>
  </footer>
</template>
