<script setup>
import '@/styles/FilterBar.css'
</script>

<template>
  <aside class="filter">
    <div class="filter__field">
      <label class="filter__label" for="sort-by">Sort by:</label>
      <select id="sort-by" class="filter__select">
        <option value="alphabetical">Alphabetical</option>
        <option value="release_date">Release Date</option>
        <option value="popularity">Popularity</option>
      </select>
    </div>

    <div class="filter__field">
      <label class="filter__label" for="order-by">Order by:</label>
      <select id="order-by" class="filter__select">
        <option value="asc">Ascending</option>
        <option value="desc">Descending</option>
      </select>
    </div>

    <div class="filter__field">
      <label class="filter__label" for="genre">Genre:</label>
      <select id="genre" class="filter__select">
        <option value="">All Genres</option>
        <option value="shooter">Shooter</option>
        <option value="mmorpg">MMORPG</option>
        <option value="arpg">ARPG</option>
        <option value="strategy">Strategy</option>
      </select>
    </div>

    <div class="filter__field">
      <label class="filter__label" for="popularity">Popularity:</label>
      <input id="popularity" class="filter__range" type="range" min="0" max="5" step="1" value="0" />
    </div>
  </aside>
</template>

<style scoped>
</style>
