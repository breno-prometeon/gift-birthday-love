<template>
  <section class="py-24 px-6 bg-gradient-to-b from-white to-pink-100 text-center">
    <!-- Mensagens -->
    <h2
      v-for="(mensagem, index) in mensagens"
      :key="index"
      :class="index === 0 ? 'text-2xl md:text-3xl font-semibold text-pink-700 mb-6 max-w-2xl mx-auto leading-snug' : 'text-4xl md:text-4xl font-semibold text-pink-800 mb-6 max-w-2xl mx-auto leading-snug'"
    >
      {{ mensagem }}
    </h2>

    <!-- Autor -->
    <p class="text-lg md:text-xl text-gray-800 mt-4">
      Com todo o meu amor, <span class="font-bold text-pink-600">{{ autor }}</span>
    </p>
  </section>
</template>

<script setup>
import { mensagens, autor } from '~/data/message.js'
</script>
