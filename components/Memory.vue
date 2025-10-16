<template>
  <section class="py-16 px-6 bg-white text-center">
    <h2 class="text-3xl md:text-4xl font-bold text-pink-700 mb-8">
      {{ titulo }}
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
      <div
        v-for="(item, index) in memorias"
        :key="index"
        class="bg-pink-100 rounded-xl shadow-md p-6 text-left border border-pink-200"
      >
        <h3 class="text-xl font-semibold text-pink-800 mb-1">
          {{ item.titulo }}
        </h3>
        <p class="text-sm text-pink-600 mb-3">{{ item.data }}</p>
        <p class="text-gray-700 text-justify">{{ item.descricao }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { titulo, memorias } from '~/data/memory.js'
</script>
