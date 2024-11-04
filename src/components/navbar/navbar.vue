<script setup>
import { useDark, useToggle } from "@vueuse/core";
import githubIcon from "@/components/icons/githubIcon.vue";

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>

<template>
  <!-- <header class="w-screen box-border overflow-x-hidden bg-white/50 dark:bg-[#171C22]/50 border-b dark:border-gray-900 z-40 fixed top-0"> -->
  <header class="w-screen box-border overflow-x-hidden z-40 fixed top-0 header-nav">
    <div class="mx-auto px-6 lg:px-8 max-w-7xl flex items-center justify-between gap-3 h-[4rem]">
      <div class="flex items-center justify-center gap-3">
        <div class="w-7 h-7 text-white bg-[#23DB85] flex items-center justify-center font-bold text-xl rounded text-white dark:text-gray-200">IH</div>
        <span class="font-bold hidden lg:block">Irul Huda</span>
      </div>
      <div class="flex items-center justify-center gap-10 text-sm lg:text-base">
        <a href="#" class="border-b-2 border-[#23DB85] text-white">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
      </div>

      <div class="flex items-center justify-center gap-3">
        <!-- <button
          @click="toggleDark()"
          type="button"
          class="group focus:outline-none focus-visible:outline-0 disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 p-1.5 hover:text-gray-700 focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 inline-flex items-center text-[#171C22]"
          aria-label="Switch to light mode"
        >
          <svg v-if="isDark" xmlns="http://www.w3.org/2000/svg" id="Layer_1" data-name="Layer 1" viewBox="0 0 24 24" class="w-5 h-5 -rotate-45 fill-current">
            <path
              d="M15,24a12.021,12.021,0,0,1-8.914-3.966,11.9,11.9,0,0,1-3.02-9.309A12.122,12.122,0,0,1,13.085.152a13.061,13.061,0,0,1,5.031.205,2.5,2.5,0,0,1,1.108,4.226c-4.56,4.166-4.164,10.644.807,14.41a2.5,2.5,0,0,1-.7,4.32A13.894,13.894,0,0,1,15,24Zm.076-22a10.793,10.793,0,0,0-1.677.127,10.093,10.093,0,0,0-8.344,8.8A9.927,9.927,0,0,0,7.572,18.7,10.476,10.476,0,0,0,18.664,21.43a.5.5,0,0,0,.139-.857c-5.929-4.478-6.4-12.486-.948-17.449a.459.459,0,0,0,.128-.466.49.49,0,0,0-.356-.361A10.657,10.657,0,0,0,15.076,2Z"
            />
          </svg>

          <svg v-else xmlns="http://www.w3.org/2000/svg" id="Layer_1" data-name="Layer 1" viewBox="0 0 24 24" class="w-5 h-5 fill-current">
            <path
              d="M12,17c-2.76,0-5-2.24-5-5s2.24-5,5-5,5,2.24,5,5-2.24,5-5,5Zm0-8c-1.65,0-3,1.35-3,3s1.35,3,3,3,3-1.35,3-3-1.35-3-3-3Zm1-5V1c0-.55-.45-1-1-1s-1,.45-1,1v3c0,.55,.45,1,1,1s1-.45,1-1Zm0,19v-3c0-.55-.45-1-1-1s-1,.45-1,1v3c0,.55,.45,1,1,1s1-.45,1-1ZM5,12c0-.55-.45-1-1-1H1c-.55,0-1,.45-1,1s.45,1,1,1h3c.55,0,1-.45,1-1Zm19,0c0-.55-.45-1-1-1h-3c-.55,0-1,.45-1,1s.45,1,1,1h3c.55,0,1-.45,1-1ZM6.71,6.71c.39-.39,.39-1.02,0-1.41l-2-2c-.39-.39-1.02-.39-1.41,0s-.39,1.02,0,1.41l2,2c.2,.2,.45,.29,.71,.29s.51-.1,.71-.29Zm14,14c.39-.39,.39-1.02,0-1.41l-2-2c-.39-.39-1.02-.39-1.41,0s-.39,1.02,0,1.41l2,2c.2,.2,.45,.29,.71,.29s.51-.1,.71-.29Zm-16,0l2-2c.39-.39,.39-1.02,0-1.41s-1.02-.39-1.41,0l-2,2c-.39,.39-.39,1.02,0,1.41,.2,.2,.45,.29,.71,.29s.51-.1,.71-.29ZM18.71,6.71l2-2c.39-.39,.39-1.02,0-1.41s-1.02-.39-1.41,0l-2,2c-.39,.39-.39,1.02,0,1.41,.2,.2,.45,.29,.71,.29s.51-.1,.71-.29Z"
            />
          </svg>

          <div class="invisible group-hover:visible fixed border border-gray-500 text-[#171C22] text-[10px] p-1 rounded" style="transform: translate(-40px, 35px)">
            {{ isDark ? "Switch to light mode" : "Switch to dark mode" }}
          </div>
        </button> -->

        <a target="_blank" href="https://github.com/irulhuda983" class="w-6 h-6 text-[#171C22]">
          <githubIcon class="text-white" />
        </a>
      </div>
    </div>
  </header>
</template>
