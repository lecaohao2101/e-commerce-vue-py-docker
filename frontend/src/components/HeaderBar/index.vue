<template lang="pug">
  div

      .header-color
        v-list-item.pa-3.center
          v-img(
          src="https://simicart.com/wp-content/uploads/eCommerce-logo.jpg"
          max-width="40"
          )
          v-spacer
          v-text-field(
            label="Search"
            placeholder="Product"
            solo
            hide-details
            background-color="white"
            prepend-inner-icon="mdi-home-search-outline"
            )
          v-spacer
          div.pa-2
            v-icon(color="white" ) mdi-home
            span.white--text Home
          div.pa-2
            v-icon(color="white" ) mdi-account
            span.white--text Account
          div.pl-10
            v-btn(icon)
              v-icon(color="white" ) mdi-cart-outline
        hr
        .center
          ul
            li.pa-5.white--text(v-for="category in categoriesTop") {{category}}

</template>

<script lang="ts">
const HeaderBar ={
  data() {
    return {
      categoriesTop:[
        "Home",
        "Featured",
        "Discount",
        "Best Seller",
        "New Product",
        "Products by Brand"
      ]
    }
  }
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
ul li
  list-style: none
  display: inline-block
  margin: 0 3px
ul li:hover
  background-color: #faabcd
  cursor: pointer



</style>