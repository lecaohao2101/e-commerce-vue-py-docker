<template lang="pug">
  div
    header-bar
    .max-width.center
      v-row.pt-10.hidden-sm-and-down
        v-col(cols="2")
          categories
        v-col(cols="8")
          carousel(:is-mobile="false")
          h1.color-main.pt-5 Welcome to website
        v-col(cols="2")
          v-img(src="https://t3.ftcdn.net/jpg/04/65/46/52/360_F_465465254_1pN9MGrA831idD6zIBL7q8rnZZpUCQTy.jpg")
      carousel.mt-3.hidden-md-and-up(:is-mobile="true")
      h1.color-main.hidden-md-and-up Welcome to website

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
.color-main
  color: #f57e2e

</style>