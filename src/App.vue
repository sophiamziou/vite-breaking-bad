<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppSelect from "./components/AppSelect.vue";
import Results from "./components/Results.vue";
import { store } from "./store.js";

export default {
  components: {
    AppHeader,
    AppMain,
    AppSelect,
    Results,
  },
  data() {
    return {
      store,
    };
  },
  created() {
    this.getCards();
  },

  methods: {
    getCards() {
      let myUrl = `${store.url}${store.selectedGenre}`;
      axios.get(myUrl).then((response) => {
        store.charactersList = response.data.data;
        setTimeout(() => {
          store.loading = false;
        }, 100);
      });
    },
  },
};
</script>

<template>
  <AppHeader></AppHeader>
  <main>
    <AppSelect @filter="getCards"></AppSelect>
    <Results></Results>
    <AppMain></AppMain>
  </main>
</template>

<style lang="scss">
@use "./styles/partials/variables" as *;
@use "./styles/generals.scss" as *;
main {
  padding: 10px 60px;
  background-color: $brown-color;
}
</style>
