<script>

import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";
import axios from "axios";
import { store } from "./Store";

export default {
    data() {
        return {
          store,
          // myurl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
          // cards: [],
        };
    },
    components: {
        AppHeader,
        AppMain,
        AppFooter
    },  
    methods: {

    },
    created() {
        axios
            .get(this.store.myurl)
            .then((response) => {
                // console.log(response.data);
                // this.cards.push(response.data);
                this.store.cards = response.data.data;
                console.log(this.store.cards);
            });
    }
}
</script>

<template>
  <div>

    <AppHeader />
    <AppMain />
    <!-- <AppFooter /> -->
  </div>
</template>

<style lang="scss">
@use "assets/scss/main" as *;
@import "assets/scss/partials/reset";
</style>
