<script setup>
import '@/styles/GameCard.css'

const props = defineProps({
  game: {
    type: Object,
    required: true,
  },
})

const maxGenres = 2
</script>

<template>
  <article class="card">
    <img class="card__image" :src="game.thumbnail" :alt="game.title" />
    <section class="card__content">
      <header class="card__header">
        <h2 class="card__title line-clamp-1">{{ game.title }}</h2>
      </header>
      <p class="card__description line-clamp-3">{{ game.short_description }}</p>
      <footer class="card__footer">
        <ul class="card__genres">
          <li v-for="genre in game.genre.slice(0, maxGenres)" :key="genre">
            <span class="card__badge has-background-blue has-text-white">{{ genre }}</span>
          </li>
        </ul>
        <time class="card__badge has-background-grey has-text-white" :datetime="game.release_date">
          {{ game.release_date }}
        </time>
      </footer>
    </section>
  </article>
</template>

<style scoped>
</style>
