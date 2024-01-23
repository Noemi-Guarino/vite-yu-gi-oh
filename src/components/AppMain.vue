<script>
import Appsinglecard from './Appsinglecard.vue';
import axios from 'axios';
import { store } from '../store';

export default {
    data() {
        return {
          store
        };
    },
    methods: {
      filtercards(){
        axios 
          .get(this.store.myurl+"&archetype="+this.store.searcharchetype)
          .then((response) => {
              // console.log(response.data);
              // this.cards.push(response.data);
              this.store.cards = response.data.data;
              console.log(this.store.cards);
          });
      }
    }, 
    components:{
      Appsinglecard
    },
    // props: {
    //   allcards: Object
    // }
}
</script>

<template>
    <main>
      <div class="container p-4">
        <div class="row p-4">
          <div class="col">
            <form>
              <select v-model="store.searcharchetype" @change="filtercards" name="" id="">
                <option value="Select archetype"> Select archetype </option>
                <option value="Alien"> Alien </option>
                <option value="Archfiend"> Archfiend </option>
                <option value="Noble Knight"> Noble Knight </option>
                <option value="Infernoble Arms"> Infernoble Arms </option>
                <option value="Melodious"> Melodious </option>
              </select>
            </form>
          </div>
        </div>
      </div>
      <div class="container p-4 mb-3">
        <div class="row">
          <div class="col-lg-3 col-md-6 col-sm-2 mb-2" v-for="(card,index) in store.cards">
            <Appsinglecard :card="card"/>
            <!-- <div class="singlecard mb-4">
              <div class="container_img  mb-2">
                <img :src="card.card_images[0].image_url" :alt="card.name" srcset="">
              </div>
              <div class="info ">
                <h3>{{ card.name }}</h3>
                <h5>{{ card.archetype }}</h5>
              </div>
            </div> -->
          </div>    
        </div>
      </div>
</main>
</template>

<style lang="scss" scoped>

</style>
