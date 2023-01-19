<script lang="js">
import AppCard from "./AppCard.vue";
import AppSelect from "./AppSelect.vue";
import { store } from "../store.js";

export default {
  components: {
    AppCard,
    AppSelect,
  },
  data() {
    return {
      store,
    };
  },
};
</script>
<template lang="">
  <div class="container">
    <AppCard
      v-for="(item, index) in store.charactersList"
      :key="index"
      :character="item"
    />
  </div>
</template>
<style lang="scss">
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins" as *;
.container {
  background-color: white;
  height: 500px;
}
</style>
