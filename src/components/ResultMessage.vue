<script>
import { store } from "../store";

export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="result-message">Found {{ store.characterList.length }} cards</div>
</template>

<style lang="scss" scoped>
.result-message {
  padding: 1rem;
  font-weight: bold;
  background-color: #212529;
  color: white;
}
</style>
