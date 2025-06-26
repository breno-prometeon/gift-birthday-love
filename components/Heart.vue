<template>
  <div class="fixed top-0 left-0 w-full h-full pointer-events-none overflow-hidden z-0">
    <div
      v-for="n in 4"
      :key="n"
      class="absolute text-pink-400 text-xl animate-heart"
      :style="randomStyle()"
    >
      ❤️
    </div>
  </div>
</template>

<script setup>
function randomStyle() {
  const left = Math.random() * 100
  const delay = Math.random() * 5
  const duration = 5 + Math.random() * 5
  const size = 16 + Math.random() * 16

  return {
    left: `${left}%`,
    animationDelay: `${delay}s`,
    animationDuration: `${duration}s`,
    fontSize: `${size}px`,
  }
}
</script>

<style scoped>
@keyframes heart-fall {
  0% {
    transform: translateY(-100px) rotate(0deg);
    opacity: 1;
  }
  100% {
    transform: translateY(100vh) rotate(360deg);
    opacity: 0;
  }
}

.animate-heart {
  animation-name: heart-fall;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
}
</style>
