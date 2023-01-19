<script>
export default {
  props: {
    character: Object,
  },
};
</script>
<template lang="">
  <div>
    <img :src="character.card_images[0].image_url" :alt="character.name" />
    <div>
      <h2>Rarity: {{ character.card_sets[0].set_rarity }}</h2>
    </div>
    <div>
      Amazon Price:
      <h4>{{ character.card_prices[0].amazon_price }}</h4>
    </div>
    <h6>{{ character.name }}</h6>
    <span>{{ character.archetype }}</span>
  </div>
</template>
<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;
</style>
