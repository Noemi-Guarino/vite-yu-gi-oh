<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';

export default {
    data() {
        return {
          myurl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0',
          cards: [ ],
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
            .get(this.myurl)
            .then((response) => {
                // console.log(response.data);
                // this.cards.push(response.data);
                this.cards = response.data;
                console.log(this.cards);
            });
    }
}
</script>

<template>
  <div>

    <AppHeader />
    <AppMain :allcards="cards" />
    <AppFooter />
  </div>
</template>

<style lang="scss">
@use "assets/scss/main" as *;
@import "assets/scss/partials/reset";
</style>
