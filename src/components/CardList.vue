<script setup>
import '@/styles/CardList.css'
import GameCard from './GameCard.vue'

defineProps({
  games: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <section class="card-list">
    <GameCard v-for="game in games" :key="game.id" :game="game" />
  </section>
</template>

<style scoped>
</style>
