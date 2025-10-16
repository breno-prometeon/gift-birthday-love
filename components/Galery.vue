<template>
  <section class="py-16 px-6 bg-pink-50 text-center">
    <h2 class="text-3xl md:text-4xl font-bold text-pink-700 mb-8">
      {{ titulo }}
    </h2>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 max-w-6xl mx-auto">
      <div v-for="(foto, index) in fotos" :key="index" class="bg-white shadow-md rounded-lg overflow-hidden">
        <img :src="foto.src" class="w-full h-64 object-cover" />
        <p class="p-4 text-gray-700 text-justify">
          {{ foto.legenda }}
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { titulo, fotos } from '~/data/galery.js'
</script>
