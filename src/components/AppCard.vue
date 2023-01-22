<script>
export default {
  props: {
    character: Object,
  },
};
</script>
<template lang="">
  <div class="card">
    <h5 class="card-title">{{ character.name }}</h5>
    <img :src="character.card_images[0].image_url" :alt="character.name" />
    <div class="card-desc">
      <h2>{{ character.name }}</h2>
      <h4>{{ character.archetype }}</h4>
      <div>
        Amazon Price:
        <h4>{{ character.card_prices[0].amazon_price }}&euro;</h4>
      </div>
      <h5>Rarity: {{ character.card_sets[0].set_rarity }}</h5>
      <h5>Info:</h5>
      <p class="info">
        {{ character.desc }}
      </p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;
@use "../styles/generals.scss" as *;
.info {
  font-size: 15px;
  max-height: 100px;
  overflow: scroll;
}
</style>
