<script>
import AppSearch from "./components/AppSearch.vue";
import CharacterList from "./components/CharacterList.vue";
import axios from "axios";
import { store } from "./store";

export default {
  data() {
    return {
      store,
    };
  },
  components: {
    AppSearch,
    CharacterList,
  },
  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((response) => (this.store.characterList = response.data.results));
  },
};
</script>

<template>
  <h1>Yu-Gi-Oh Api</h1>
  <AppSearch />
  <CharacterList />
</template>

<style lang="scss"></style>
