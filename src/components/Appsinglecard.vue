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
      <div class="singlecard">
        <div class="container_img mb-4">
          <img class="w-100 h-100" :src="card.card_images[0].image_url" :alt="caname" srcset="">
        </div>
        <div class="info">
          <h3>{{ card.name }}</h3>
          <h5>{{ card.archetype }}</h5>
        </div>
      </div>
</main>
</template>

<style lang="scss" scoped>

</style>
