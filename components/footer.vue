<template>
  <footer class="flex flex-col gap-16 mx-8 mt-16">
    <div class="flex flex-col gap-8">
      <h2 class="text-xl font-kaushan">Contact</h2>

      <UInput v-model="fullName" placeholder="First, Last Name" variant="outline" />

      <UInput v-model="preferredName" placeholder="Preferred Name" variant="outline" />

      <UInput v-model="phoneNumber" placeholder="Phone Number" variant="outline" />

      <UInput v-model="emailAddress" placeholder="Email" variant="outline" />

      <UTextarea v-model="description" placeholder="Description" variants="outline" />

      <UTextarea v-model="daysAndTimes" placeholder="Preferred Days and Times" variants="outline" />

      <div class="flex flex-col justify-center items-center w-full py-6 rounded bg-gray-200">
        <p>Recaptcha placeholder</p>
      </div>

      <UButton class="justify-center py-4" label="Send" color="primary" variant="solid" />
    </div>

    <div class="flex flex-row gap-4 justify-center items-center">
      <div class="w-1/2">
        <p>Hannah Thayer, LPCC</p>
        <p>Remote in California</p>
      </div>

      <div class="w-1/2 bg-gray-200 py-6 flex justify-center">
        <p>logo</p>
      </div>
    </div>

    <div class="flex flex-col justify-center items-center gap-4 mb-16">
      <p>Copyright © 2024 • Hannah Thayer</p>

      <p>Created by <a class="" target="_blank" href="https://dalechang.me">Dale Chang</a></p>
    </div>
  </footer>
</template>


<script setup>

import { ref } from 'vue';

const fullName = ref('');
const preferredName = ref('');
const phoneNumber = ref('');
const emailAddress = ref('');
const description = ref('');
const daysAndTimes = ref('');

</script>


<style scoped>
div {
  font-family: Roboto, sans-serif;
}
</style>