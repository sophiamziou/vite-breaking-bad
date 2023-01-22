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
    <h2 id="result">TROVATE {{ store.charactersList.length }} CARTE</h2>
  </div>
</template>
<style lang="scss">
#result {
  text-align: center;
  margin: 20px 0;
  color: white;
}
</style>
