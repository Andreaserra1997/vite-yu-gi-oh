<script>
import CharacterList from "./components/CharacterList.vue";
import ResultMessage from "./components/ResultMessage.vue";
import axios from "axios";
import { store } from "./store";

export default {
  data() {
    return {
      store,
    };
  },
  components: {
    CharacterList,
    ResultMessage,
  },
  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0")
      .then((response) => (this.store.characterList = response.data.data));
  },
};
</script>

<template>
  <h1>Yu-Gi-Oh Api</h1>
  <ResultMessage />
  <CharacterList />
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
