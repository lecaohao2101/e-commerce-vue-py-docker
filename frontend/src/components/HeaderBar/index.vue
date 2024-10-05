<template lang="pug">
  div

      .header-color
        v-list-item.pa-3.center
          v-img.hidden-md-and-down(
          src="https://simicart.com/wp-content/uploads/eCommerce-logo.jpg"
          max-width="40"
          )
          v-spacer
          v-text-field.hidden-md-and-down(
            label="Search"
            placeholder="Product"
            solo
            hide-details
            background-color="white"
            prepend-inner-icon="mdi-home-search-outline"
            )
          v-text-field.hidden-md-and-up(
            label="Search"
            placeholder="Product"
            solo
            hide-details
            background-color="white"
            prepend-inner-icon="mdi-home-search-outline"
            )
          v-spacer
          div.pa-2
            v-icon(color="white") mdi-home
            span.white--text.hidden-md-and-down Home
          div.pa-2
            v-icon(color="white") mdi-account
            span.white--text.hidden-md-and-down Account
          div.pl-10
            v-btn(icon)
              v-icon(color="white") mdi-cart-outline
          div.hidden-md-and-up
            v-icon(color="white" @click="isShowCategoryInMobile = !isShowCategoryInMobile") mdi-menu
        hr
        .pc.center.hidden-md-and-down
          ul
            li.pa-5.white--text(v-for="category in categoriesTop") {{category}}
        .center.hidden-md-and-up
          v-expand-transition
            v-card(
              color="transparent"
              v-show="isShowCategoryInMobile"
            )
              ul
                li.pa-5.white--text(v-for="category in categoriesTop") {{category}}
</template>

<script lang="ts">
const HeaderBar ={
  data() {
    return {
      isShowCategoryInMobile: false,
      categoriesTop:[
        "Home",
        "Featured",
        "Discount",
        "Best Seller",
        "New Product",
        "Products by Brand"
      ]
    }
  },

}

export default HeaderBar
</script>

<style scoped lang="sass">
.header-color
  background-color: #f57e2e

.center
  margin: 0 auto
  text-align: center

ul
  justify-content: center
  padding: 0

ul li
  list-style: none
  margin: 0 3px

.pc ul li
    display: inline-block

ul li:hover
  background-color: #e19669
  cursor: pointer



</style>