<template>
  <footer class="py-6 bg-pink-200 text-center text-sm text-pink-900">
    <!-- Mensagem principal -->
    <p>
      <span v-for="(linha, index) in mensagem" :key="index">
        {{ linha }}<br/>
      </span>
    </p>

    <!-- Observação -->
    <span v-for="(linha, index) in observacao" :key="'obs-'+index">
      {{ linha }}
    </span>
    <br/>

    <!-- Direitos reservados -->
    © {{ new Date().getFullYear() }} – Todos os direitos reservados
  </footer>
</template>

<script setup>
import { mensagem, observacao } from '~/data/footer.js'
</script>
