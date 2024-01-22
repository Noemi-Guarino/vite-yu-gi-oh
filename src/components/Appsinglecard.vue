<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    },
    props: {
      allcards: Object
    }
}
</script>

<template>
    <main>
      <div class="container text-center">
        <div class="row text-center">
          <div class="col-3" v-for="(card,index) in allcards.data">
            <div class="singlecard mb-4">
              <div class="container_img  mb-2">
                <img :src="card.card_images[0].image_url" :alt="card.name" srcset="">
              </div>
              <div class="info ">
                <h3>{{ card.name }}</h3>
                <h5>{{ card.archetype }}</h5>
              </div>
            </div>
          </div>    
        </div>
      </div>
</main>
</template>

<style lang="scss" scoped>
  .singlecard{
    border: 2px solid blue;
  }

  .container_img{
    height: 200px;
    width: 200px;
  }
</style>
