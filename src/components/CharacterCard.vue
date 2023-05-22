<script>
export default {
  props: {
    characterData: Object,
  },
};
</script>

<template>
  <div class="card">
    <img :src="characterData.card_images[0].image_url_small" alt="" />
    <h2>{{ characterData.name }}</h2>
    <div class="archetype">{{ characterData.archetype }}</div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  text-align: center;
  background-color: #d48f38;
  padding: 1rem;
}
</style>
