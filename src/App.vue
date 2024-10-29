<template>
  <div id="app" class="container">
    <GameList :games="games" @delete-game="removeGame" />
  </div>
</template>

<script>
import Vue from 'vue';
import GameList from './components/GameList.vue';

export default Vue.extend ({
  name: 'App',
  components: {
    GameList
  },
  data() {
    return {
      games: ["Arena of valor", "Pokemon Unite", "Donkey Kong", "Heroes of the storm", "Valorant"]
    };
  },
  methods: {
    removeGame(index) {
      this.games.splice(index, 1);
    }
  }
});
</script>

<style>

</style>
