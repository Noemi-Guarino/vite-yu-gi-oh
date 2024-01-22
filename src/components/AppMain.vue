<script>
import Appsinglecard from './Appsinglecard.vue';
import { store } from '../Store'

export default {
    data() {
        return {
          store
        };
    },
    methods: {

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
