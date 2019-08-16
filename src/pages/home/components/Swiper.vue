<template>
  <div class="wrapper">     
    <swiper :options="swiperOption">
    <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl"/>
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>  
</template>

<script>
export default {
    name:'HomeSwiper',
    data () {
      return {
        swiperOption: {
          pagination:'.swiper-pagination',
          loop:true
        },
        swiperList:[{
            id:'0001',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/d7bbc21db442366a882e04ddc984669a.jpg_750x200_85e640d9.jpg'
        },{
            id:'0002',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/bd58cd26d9b642e600fa8e30bfb476f9.jpg_750x200_86e8d193.jpg'
        },{
            id:'0003',
            imgUrl:'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20196/b48d1ce6662a905d993635b4e28ff089.jpg_750x200_1c00b2f0.jpg'
        }]
      }
    }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background:#fff
.wrapper
  overflow:hidden
  width:100%
  height:0
  padding-bottom:26.7%
  .swiper-img
    width:100%
</style>
