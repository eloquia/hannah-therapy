<template>
  <div v-if="isShowBanner" class="w-full flex flex-col justify-center items-center pb-5 bg-amber-600">
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

    <div>
      <p class="text-slate-100">now accepting clients!</p>
      <p class="text-slate-100">Click here to schedule</p>
    </div>
  </div>

  <div class="flex flex-col justify-center items-center">
    <h1 class="font-kaushan text-3xl text-center">VIRTUAL THERAPY FOR ADULTS IN CALIFORNIA</h1>
    <p class="text-center">Affordable treatment for those going through trouble with familiy, friends, anxiety, OCD, and just general life.</p>
    <p>Hannah Thayer, LPCC</p>

    <NuxtImg src="/hannah-profile-photo.jpeg" sizes="300px md:400px" />

    <UButton class="justify-center py-4 px-16" label="Send" color="primary" variant="solid" />
  </div>
</template>


<script setup>

import { ref } from 'vue';

const isShowBanner = ref(true);

function handleCloseBanner() {
  isShowBanner.value = false;
}

</script>
