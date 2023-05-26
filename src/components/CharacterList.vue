<script>
import CharacterCard from "./CharacterCard.vue";
import { store } from "../store.js";

export default {
  data() {
    return {
      store,
    };
  },
  components: {
    CharacterCard,
  },
};
</script>

<template>
  <select v-model="store.arrCard">
    <option v-for="selector in store.arrCard" :key="selector.id">
      {{ selector.archetype_name }}
    </option>
  </select>
  <div class="cards-container">
    <CharacterCard
      v-for="character in store.characterList"
      :key="character.id"
      class="card-character"
      :characterData="character"
    />
  </div>
</template>

<style lang="scss" scoped>
.cards-container {
  display: flex;
  flex-wrap: wrap;
}
.card-character {
  flex: 0 0 20%;
}
</style>
