<template>
  <section class="py-16 px-6 bg-white text-center">
    <h2 class="text-3xl md:text-4xl font-bold text-pink-700 mb-8">
      Algumas Memórias 💭
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
const memorias = [
  {
    titulo: 'Nosso primeiro encontro',
    data: 'Meados de Outubro de 2023',
    descricao: 'Nesse fatídico dia, fomos comer no OutBack e o Paulo foi com a gente mas ali estavamos dando definitivamente o pontepé inicial.',
  },
  {
    titulo: 'A viagem para o litoral - Guarujá',
    data: 'Julho de 2024',
    descricao: 'Tivemos alguns contratempos por conta do clima, mas o mais importante foi que ficamos juntos e aproveitamos MUITO, foi como viver dentro de um sonho.',
  },
  {
    titulo: 'Nosso primeiro “Eu te amo”',
    data: 'Não lembro a data exata, mas foi em meados de Outubro de 2023',
    descricao: 'Duas palavras que mudaram tudo. Desde então, sempre mantenho fresca essas palavras, pois meu coração é seu, e sempre será.',
  },
  {
    titulo: 'Primeiro Ano Novo juntos',
    data: 'Dezembro de 2023',
    descricao: 'Celebramos a chegada do novo ano com abraços, risadas e promessas de um futuro juntos, todos em família, e você minha futura esposa!',
  },
  {
    titulo: 'Nosso primeiro Natal juntos',
    data: 'Dezembro de 2023',
    descricao: 'A magia do Natal ficou ainda mais especial com você ao meu lado, compartilhando risadas e amor.',
  },
  {
    titulo: 'Muitos momentos especiais',
    data: 'Até o fim',
    descricao: 'Nossa história está apenas começando, e cada dia traz novas memórias que guardaremos com carinho. Quero criar muitos mais momentos especiais com você.',
  },
]
</script>
