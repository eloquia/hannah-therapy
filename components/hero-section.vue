<template>
  <div v-if="isShowBanner" class="w-full flex flex-col justify-center items-center pb-5 bg-one-periwinkle-pink-300">
    <div class="w-full flex flex-row gap-4 justify-end">
      <UButton
        class="text-black"
        icon="i-heroicons-x-mark"
        size="sm"
        color="primary"
        variant="ghost"
        @click="handleCloseBanner"
      />
    </div>

    <div @click="navigateToSchedule">
      <p class="text-zinc-900">Now accepting clients!</p>
      <p class="text-zinc-900">Click here to schedule</p>
    </div>
  </div>

  <div class="flex flex-col justify-center items-center mt-16 px-8">
    <h1 class="text-3xl text-center mb-4">VIRTUAL THERAPY FOR ADULTS IN CALIFORNIA</h1>
    <p class="text-center mb-8">Affordable treatment for those going through trouble with familiy, friends, anxiety, OCD, and just general life.</p>
    <p class="mb-16">Hannah Thayer, LPCC</p>

    <NuxtImg class="mb-16" src="/hannah-profile-photo.jpeg" sizes="300px md:400px" />

    <UButton class="justify-center py-4 px-16 bg-one-periwinkle-pink-300 text-zinc-900" label="SCHEDULE CONSULTATION CALL" variant="solid" @click="navigateToSchedule" />
  </div>
</template>


<script setup>

import { ref } from 'vue';

const isShowBanner = ref(true);

function handleCloseBanner() {
  isShowBanner.value = false;
}

function navigateToSchedule() {
  console.log('navigateToSchedule')
}

</script>
