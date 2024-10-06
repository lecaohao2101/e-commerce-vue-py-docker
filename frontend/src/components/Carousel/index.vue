<template lang="pug">
  v-carousel(:height="isMobile ? 150 : 300" )
    v-carousel-item(v-for="(image, i) in images" :key="i" :src="image" reverse-transition="fade-transition" transition="fade-transition")

</template>


<script lang="ts">
const Carousel ={
  props: ['isMobile'],
  data (){
    return {
      images:[
        'https://t3.ftcdn.net/jpg/04/65/46/52/360_F_465465254_1pN9MGrA831idD6zIBL7q8rnZZpUCQTy.jpg',
        'https://giuongbenhchinhhang.vn/wp-content/uploads/2023/12/BANNER-BAN-HANG-NOEL-3-09.png',
        'https://cdn.tgdd.vn/Files/2021/11/06/1396147/1111_1280x720-800-resize.jpg'
      ]
    }
  }
}
export default Carousel
</script>



<style scoped lang="sass">

</style>