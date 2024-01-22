<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    }
}
</script>

<template>
  <div>
    <header>
      <div class="bg-page">
        <div class="container text-center">
          <div class="header_container">
            <div class="img_conteiner">
              <img class="" src="../img/Yugioh_anime_logo.webp" alt="">
            </div>    
            <div class="">
              <h1>Yu-Gi-Oh Api</h1>
            </div>    
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<style lang="scss" scoped>
.bg-page{
  height: 100px;
  background-color: white;
  // border: 1px solid red;
}

.header_container{
  display: flex;
  align-items: center;
}

.img_conteiner{
  img{
    height: 100px;
  }
}
</style>
