<template>
  <footer class="bg-slate-200 flex flex-col gap-16 px-8 pt-16">
    <div class="flex flex-col gap-8">
      <h2 class="text-xl font-kaushan">Contact</h2>

      <div class="flex flex-row gap-4">
        <UFormGroup label="First Name (required)" name="firstName" class="w-full">
          <UInput v-model="firstName" variant="outline" />
        </UFormGroup>

        <UFormGroup label="Last Name (required)" name="lastName" class="w-full">
          <UInput v-model="lastName" variant="outline" />
        </UFormGroup>
      </div>

      <UFormGroup label="Preferred Name (optional)" name="preferredName" class="w-full">
        <UInput v-model="preferredName" variant="outline" />
      </UFormGroup>

      <UFormGroup label="Email Address (required)" name="emailAddress" class="w-full">
        <UInput v-model="emailAddress" placeholder="Email" variant="outline" />
      </UFormGroup>

      <UFormGroup label="Phone Number (optional)" name="phoneNumber" class="w-full">
        <UInput v-model="phoneNumber" placeholder="Phone Number" variant="outline" />
      </UFormGroup>

      <UFormGroup label="Preferred method of contact" name="selectedContactOption">
        <USelectMenu v-model="selectedContactOption" :options="contactOptions" :popper="{ arrow: true }" />
      </UFormGroup>

      <UFormGroup label="Description (required)" name="description">
        <UTextarea v-model="description" placeholder="Description" variants="outline" />
      </UFormGroup>

      <UFormGroup label="Days and and Times (optional)" name="daysAndTimes">
        <UTextarea v-model="daysAndTimes" placeholder="Preferred Days and Times" variants="outline" />
      </UFormGroup>

      <div class="flex flex-col justify-center items-center w-full py-6 rounded bg-gray-300">
        <p>Recaptcha placeholder</p>
      </div>

      <UButton class="justify-center py-4" label="Send" color="primary" variant="solid" />
    </div>

    <div class="flex flex-row gap-4 justify-center items-center">
      <div class="w-1/2">
        <p>Hannah Thayer, LPCC</p>
        <p>Remote in California</p>
      </div>

      <div class="w-1/2 bg-gray-300 py-6 flex justify-center">
        <p>logo</p>
      </div>
    </div>

    <div>
      <nav class="flex flex-col gap-4">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>

    <div class="flex flex-col justify-center items-center gap-4 mb-16">
      <p>Copyright © 2024 • Hannah Thayer</p>

      <p>Created by <a class="" target="_blank" href="https://dalechang.me">Dale Chang</a></p>
    </div>
  </footer>
</template>


<script setup>

import { ref } from 'vue';

const contactOptions = ['Email', 'Phone Number'];

const firstName = ref('');
const lastName = ref('');
const preferredName = ref('');
const phoneNumber = ref('');
const emailAddress = ref('');
const description = ref('');
const daysAndTimes = ref('');

const selectedContactOption = ref(contactOptions[0])

</script>


<style scoped>
div {
  font-family: Roboto, sans-serif;
}
</style>