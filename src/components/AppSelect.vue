<script>
import { store } from "../store.js";
export default {
  data() {
    return {
      store,
      archetypes: ["Dark Magician", "Cipher", "Laval", "Alien"],
    };
  },
};
</script>
<template lang="">
  <div class="select">
    <select v-model="store.selectedGenre" @change="$emit('filter')">
      <option v-for="item in archetypes" :value="item">{{ item }}</option>
    </select>
  </div>
</template>
<style lang="scss">
.select {
  margin: 30px;
  select {
    border: none;
    padding: 10px;
    font-size: 15px;
  }
}
</style>
