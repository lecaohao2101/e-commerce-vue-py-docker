<template lang="pug">
  div
    header-bar
    .max-width.center
      v-row.pt-10
        v-col(cols="2")
          categories
        v-col(cols="8")
          carousel
        v-col(cols="2")
          v-img(src="https://t3.ftcdn.net/jpg/04/65/46/52/360_F_465465254_1pN9MGrA831idD6zIBL7q8rnZZpUCQTy.jpg")
      h1 day la home

</template>

<script lang="ts">
import HeaderBar from "@/components/HeaderBar/index.vue";
import Categories from "@/components/Categories/index.vue";
import Carousel from "@/components/Carousel/index.vue";
const Home ={
  components: {
    HeaderBar,
    Categories,
    Carousel

  }
}

export default Home
</script>

<style scoped lang="sass">
.max-width
  max-width: 1500px
.center
  margin: 0 10px 0 10px
  text-align: center

</style>