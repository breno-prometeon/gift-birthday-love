<template>
    <section class="py-16 px-6 bg-pink-50 text-center">
        <h2 class="text-3xl md:text-4xl font-bold text-pink-700 mb-8">
            Nossos Momentos 📸
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
    const fotos = [
        {
            src: '/img/abraco_piscina.jpg',
            legenda: 'Viagem para São Vicente 💕',
        },
        {
            src: '/img/ano_novo.jpg',
            legenda: 'Nosso primeiro ano novo juntos 🎉',
        },
        {
            src: '/img/aparecida.jpg',
            legenda: 'Viagem para Aparecida do Norte 🙏',
        },
        {
            src: '/img/beijo_piscina.jpg',
            legenda: 'Na piscina com a sereia 💦',
        },
        {
            src: '/img/bruxinha.jpg',
            legenda: 'Minha bruxinha 🧙‍♀️',
        },
        {
            src: '/img/casamento.jpg',
            legenda: 'Casamento da Bih 💍',
        },
        {
            src: '/img/elevador.jpg',
            legenda: 'Foto no elevador só para registrar 🚪',
        },
        {
            src: '/img/espontanea.jpg',
            legenda: 'Uma fotinha espontânea 😄',
        },
        {
            src: '/img/igreja_bobeira.jpg',
            legenda: 'Na Igreja não pode faltar 😜',
        },
        {
            src: '/img/marinete.jpg',
            legenda: 'Viagem para tia Marinete 👵',
        },
        {
            src: '/img/piscina.jpg',
            legenda: 'Mais um dia de piscina 🏊‍♂️',
        },
        {
            src: '/img/praia.jpg',
            legenda: 'Curtindo a prainha 🏖️',
        },
        {
            src: '/img/primeira_viagem.jpg',
            legenda: 'Nossa primeira viagem juntos ✈️',
        },
        {
            src: '/img/primeiro_ano.jpg',
            legenda: 'Comemorando o primeiro ano 🎂',
        },
        {
            src: '/img/rodizio.jpg',
            legenda: 'Rodízio 🍣',
        },
        {
            src: '/img/sao_vicente.jpg',
            legenda: 'Passeio em São Vicente 🌊',
        },
        {
            src: '/img/viagem_amigos.jpg',
            legenda: 'Viagem com amigos 👯‍♂️',
        },
        {
            src: '/img/milionario.jpg',
            legenda: 'Aquele dia no clube dos bancários 🏊‍♂️',
        },
    ]
</script>
