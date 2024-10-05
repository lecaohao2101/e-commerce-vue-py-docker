<template lang="pug">
  .border.width-card
    //v-card.mx-auto(max-width="300" title="")
    v-list(dense="")
      v-subheader SP Noi Bat
      v-list-item-group(v-model="selectedItem" color="#e19669")
        v-list-item(v-for='(item, i) in items' :key='i')
          v-img(:src="item.icon" max-width="30px")
          span.pl-4 {{item.text}}
</template>


<script lang="ts">
const Categories = {
  data() {
    return {
      selectedItem: 1,
      items: [
        { text: 'Airpods', icon: '' },
        { text: 'Apple Watch', icon: 'mdi-account' },
        { text: 'Book', icon: 'https://www.novelkicks.co.uk/wp-content/uploads/2013/05/leather-book-preview.png' },
        { text: 'Cosmetics', icon: 'https://png.pngtree.com/png-vector/20240818/ourmid/pngtree-geset-of-luxury-beauty-cosmetic-makeup-bdifferent-png-image_13532167.png' },
        { text: 'Clothes', icon: '' },
        { text: 'Glasses', icon: '' },
        { text: 'Gadgets', icon: 'mdi-account' },
        { text: 'Handbags', icon: 'mdi-flag' },
        { text: 'Ipad', icon: 'mdi-flag' },
        { text: 'Kid\'s Fashion', icon: 'mdi-account' },
        { text: 'Laptop', icon: '' },
        { text: 'Men\'s Fashion', icon: 'mdi-account' },
        { text: 'Sports', icon: 'mdi-flag' },
        { text: 'PC', icon: 'mdi-clock' },
        { text: 'Toys', icon: 'mdi-account' },
        { text: 'Woman\'s Fashion', icon: 'mdi-account' },




      ],
    }
  }
}

export default Categories
</script>




<style scoped lang="sass">

.border
  //border-radius: 15px
  border: 2px solid
  color: #f57e2e
.width-card
  max-width: 250px

</style>