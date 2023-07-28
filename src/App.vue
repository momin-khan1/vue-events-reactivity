<script setup>
import { ref } from 'vue';

const location = ref("Dhaka");
const changeLocation = (newLocation) => {
  location.value = newLocation;
};

const changeButtonColor = ref("bg-sky-400");
</script>

<template>
  <section class="container mx-auto flex items-center flex-col">
    <h1 class="text-center text-2xl py-10">Events & Reactivity in Vue.js</h1>
    <div class="container mx-auto flex space-x-5 justify-center m-5">
      <button
        @click="changeLocation('Dhaka')"
        class="text-white font-bold py-2 px-4 rounded"
        :class="changeButtonColor"
      >
        Dhaka
      </button>
      <button
        @click="changeLocation('Rajshahi')"
        class="text-white font-bold py-2 px-4 rounded"
        :class="changeButtonColor"
      >
        Rajshahi
      </button>
      <button
        @click="changeLocation('Khulna')"
        class="text-white font-bold py-2 px-4 rounded"
        :class="changeButtonColor"
      >
        Khulna
      </button>
    </div>
    <h1 class="text-2xl m-10">Current Location is {{ location }}</h1>
    <div class="mt-10 space-x-8 flex justify-center">
      <div @click="changeButtonColor = 'bg-orange-400'" class="flex w-14 h-14 bg-orange-400 cursor-pointer"></div>
      <div @click="changeButtonColor = 'bg-red-400'" class="flex w-14 h-14 bg-red-400 cursor-pointer"></div>
      <div @click="changeButtonColor = 'bg-sky-400'" class="flex w-14 h-14 bg-sky-400 cursor-pointer"></div>
    </div>
  </section>
</template>

<style scoped></style>
