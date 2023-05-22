<script>
export default {
  props: {
    characterData: Object,
  },
};
</script>

<template>
  <h2>{{ characterData.name }}</h2>
  <div class="title"></div>
  <div class="archetype"></div>
</template>

<style lang="scss" scoped></style>
