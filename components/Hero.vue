<template>
  <section class="h-screen flex flex-col items-center justify-center text-center bg-gradient-to-b from-pink-100 to-white px-4">
    <div class="w-32 h-32 md:w-40 md:h-40 rounded-full overflow-hidden shadow-lg mb-6 border-4 border-pink-300">
      <img
        :src="foto"
        alt="Foto dela"
        class="w-full h-full object-cover"
      />
    </div>

    <h1 class="text-4xl md:text-5xl font-extrabold text-pink-700 mb-2">
      Feliz aniversário, MEU AMOR TODO! ❤️
    </h1>

    <p class="text-base md:text-lg text-gray-700 mb-6 max-w-xl">
      Hoje é o seu dia e eu só quero mostrar um pouco o quanto você é especial em minha vida, linda e única. ✨
    </p>

    <button
      @click="startTribute()"
      class="bg-pink-600 hover:bg-pink-700 text-white font-semibold py-2 px-6 rounded-full shadow-md transition duration-300"
    >
      Sobre nós
    </button>

    <audio ref="player" :src="musica" />
  </section>
</template>

<script setup>
const nome = 'Radija';
const foto = '/img/radija.jpg';
const musica = '/music/homenagem.mp3' 
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
