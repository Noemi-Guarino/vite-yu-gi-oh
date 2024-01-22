<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    },
    props: {
      card: Object
    }
}
</script>

<template>
    <main>
      <div class="singlecard mb-4">
        <div class="container_img  mb-2">
          <img :src="card.card_images[0].image_url" :alt="caname" srcset="">
        </div>
        <div class="info ">
          <h3>{{ card.name }}</h3>
          <h5>{{ card.archetype }}</h5>
        </div>
      </div>
</main>
</template>

<style lang="scss" scoped>
  .singlecard{
    border: 2px solid blue;
  }

  .container_img{
    height: 150px;
    width: 150px;
  }
</style>
