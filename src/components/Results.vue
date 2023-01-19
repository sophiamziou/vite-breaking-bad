<script>
import { store } from "../store";
export default {
  data() {
    return {
      store,
    };
  },
  computed: {
    numberResults() {
      return store.charactersList.length;
    },
  },
};
</script>
<template>
  <div>
    <h4>Trovate {{ store.charactersList.length }} carte</h4>
  </div>
</template>
<style lang=""></style>
