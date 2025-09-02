<script setup>
  import ClockDisplay from './components/ClockDisplay.vue';
</script>

<template>
  <header class="pt-20 pb-10">
    <h1 class="text-center text-4xl font-capsule tracking-widest">
      Universal Watch
    </h1>
  </header>

  <main class="mt-10 mb-20 px-8">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-20">
      <div class="flex flex-col items-center justify-center gap-6 col-span-full">
        <ClockDisplay class="text-white">
        </ClockDisplay>
        <h2 class="text-white text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          {{ currentTimezone }} Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-red-700" time-zone="UTC">
        </ClockDisplay>
        <h2 class="text-red-700 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          UTC Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-yellow-500" time-zone="EST">
        </ClockDisplay>
        <h2 class="text-yellow-500 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          EST Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-emerald-500" time-zone="PST">
        </ClockDisplay>
        <h2 class="text-emerald-500 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          PST Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-sky-500" time-zone="GMT">
        </ClockDisplay>
        <h2 class="text-sky-500 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          GMT Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-purple-500" time-zone="CET">
        </ClockDisplay>
        <h2 class="text-purple-500 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          CET Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-rose-500" time-zone="Asia/Dubai">
        </ClockDisplay>
        <h2 class="text-rose-500 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          GST Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-orange-700" time-zone="IST">
        </ClockDisplay>
        <h2 class="text-orange-700 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          IST Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-lime-400" time-zone="CST">
        </ClockDisplay>
        <h2 class="text-lime-400 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          CST Timezone
        </h2>
      </div>
      <div class="flex flex-col items-center justify-center gap-6">
        <ClockDisplay class="text-slate-400" time-zone="JST">
        </ClockDisplay>
        <h2 class="text-slate-400 text-center text-4xl text-shadow-[0_0_10px] text-shadow-current font-capsule tracking-widest">
          JST Timezone
        </h2>
      </div>
    </div>
  </main>

  <footer class="my-10 px-4 font-capsule tracking-widest">
    <div class="container mx-auto">
      <hr class="opacity-25 mb-8">
      <p class="text-center text-2xl">
        Copyright © 2025 All Rights Reserved -
        <a href="https://github.com/Mahmoud217TR" target="__blank"
          class="hover:text-amber-400 hover:text-shadow-[0_0_10px] hover:text-shadow-current transition-colors duration-300">
          MahmoudTR
        </a>
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      currentTimezone: Intl.DateTimeFormat().resolvedOptions().timeZone,
    }
  },
}
</script>
