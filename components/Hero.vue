<template>
  <section class="h-screen flex flex-col items-center justify-center text-center bg-gradient-to-b from-pink-100 to-white px-4">
    <!-- Foto -->
    <div class="w-32 h-32 md:w-40 md:h-40 rounded-full overflow-hidden shadow-lg mb-6 border-4 border-pink-300">
      <img
        :src="foto"
        :alt="`Foto de ${nome}`"
        class="w-full h-full object-cover"
      />
    </div>

    <!-- Título -->
    <h1 class="text-4xl md:text-5xl font-extrabold text-pink-700 mb-2">
      {{ titulo }}
    </h1>

    <!-- Descrição -->
    <p class="text-base md:text-lg text-gray-700 mb-6 max-w-xl">
      {{ descricao }}
    </p>

    <!-- Botão -->
    <button
      @click="startTribute()"
      class="bg-pink-600 hover:bg-pink-800 text-white font-semibold py-2 px-6 rounded-full shadow-md transition duration-600"
    >
      Clique aqui
    </button>

    <audio ref="player" :src="musica" />
  </section>

  <Heart />
</template>

<script setup>
import { nome, foto, musica, titulo, descricao } from '~/data/hero.js'
import { ref } from 'vue'

const player = ref(null)

function startTribute() {
  if (player.value) {
    player.value.play().catch((e) => {
      console.warn('Autoplay bloqueado:', e)
    })
  }

  setTimeout(() => {
    const el = document.getElementById('sobre')
    if (el) el.scrollIntoView({ behavior: 'smooth' })
  }, 300)
}
</script>
