<script setup>
import '@/styles/App.css'
import Header from './components/Header.vue'
import SearchBox from './components/SearchBox.vue'
import FilterBar from './components/FilterBar.vue'
import CardList from './components/CardList.vue'

const sampleGames = [
  {
    id: '540',
    title: 'Overwatch',
    thumbnail: 'https://www.freetogame.com/g/540/thumbnail.jpg',
    short_description: 'A hero-focused first-person team shooter from Blizzard Entertainment.',
    genre: ['Shooter', 'Action', 'Multiplayer'],
    platform: ['PC', 'PlayStation', 'Xbox'],
    developer: 'Blizzard Entertainment',
    release_date: '2022-10-04',
    popularity: 4,
  },
  {
    id: '516',
    title: 'PUBG: Battlegrounds',
    thumbnail: 'https://www.freetogame.com/g/516/thumbnail.jpg',
    short_description: 'Get into the action in one of the longest running free-to-play battle royale games.',
    genre: ['Shooter', 'Battle Royale'],
    platform: ['PC', 'PlayStation', 'Xbox'],
    developer: 'PUBG Corporation',
    release_date: '2022-01-12',
    popularity: 4,
  },
  {
    id: '508',
    title: 'Enlisted',
    thumbnail: 'https://www.freetogame.com/g/508/thumbnail.jpg',
    short_description: 'Get ready to command your own World War II military squad in Gaijin and Darkflow Software\'s MMO squad-based shooter.',
    genre: ['Shooter', 'MMO'],
    platform: ['PC', 'PlayStation', 'Xbox'],
    developer: 'Darkflow Software',
    release_date: '2021-04-08',
    popularity: 3,
  },
  {
    id: '556',
    title: 'FragPunk',
    thumbnail: 'https://www.freetogame.com/g/556/thumbnail.jpg',
    short_description: 'A free-to-play 5v5 hero shooter that uses cards to modify matches.',
    genre: ['Shooter', 'Action'],
    platform: ['PC', 'Xbox'],
    developer: 'Bad Guitar Studio',
    release_date: '2025-03-06',
    popularity: 4,
  },
  {
    id: '553',
    title: 'Throne And Liberty',
    thumbnail: 'https://www.freetogame.com/g/553/thumbnail.jpg',
    short_description: 'A free-to-play multi-platform MMORPG from NCSoft and Amazon Games.',
    genre: ['MMORPG', 'Adventure'],
    platform: ['PC', 'PlayStation', 'Xbox'],
    developer: 'NCSoft',
    release_date: '2024-10-01',
    popularity: 5,
  },
  {
    id: '523',
    title: 'Fall Guys',
    thumbnail: 'https://www.freetogame.com/g/523/thumbnail.jpg',
    short_description: 'Play the most competitive massively multiplayer party royale game featuring beans ever for free on a variety of platforms.',
    genre: ['Battle Royale', 'Party'],
    platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
    developer: 'Mediatonic',
    release_date: '2020-08-04',
    popularity: 4,
  },
]
</script>

<template>
  <Header />
  <main class="container main-grid">
    <div class="main-grid__top">
      <SearchBox />
      <button class="button" type="button">Reset filters</button>
    </div>
    <div class="main-grid__filterbar">
      <FilterBar />
    </div>
    <div class="main-grid__cardlist">
      <CardList :games="sampleGames" />
    </div>
  </main>
</template>

<style scoped>
</style>
