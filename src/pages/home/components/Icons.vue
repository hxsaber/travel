<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for="(page,index) of pages" 
                          :key="index">
                <div class="icon" 
                     v-for="item of page" 
                     :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" 
                             :src="item.imgUrl">
                    </div>    
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
    
</template>

<script>
export default {
    name:'HomeIcons',
    props: {
        list: Array
    },
    data () {
        return {
            swiperOption: {
                autoplay: false
            }
        }
    },
    computed:{
        // 将iconList按每8个为一大组进行轮播循环，超过8的在第二页轮播图
        pages () {
            const pages = []
            this.list.forEach((item,index) => {
                const page = Math.floor(index / 8)
                if (!pages[page]) {
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
.icons
  width:100%
  overflow:hidden
  height:0
  padding-bottom:50%
  .icon
    position:relative
    overflow:hidden
    float:left
    width:25%
    height:0
    padding-bottom:25%
    .icon-img
      position:absolute
      top:0 
      left:0
      right:0
      bottom:.44rem
      box-sizing:border-box
      padding:.17rem
      .icon-img-content
        display:block
        margin:0 auto
        height:100%    
    .icon-desc
      position:absolute
      left:0
      right:0
      bottom:.2rem
      height:.44rem
      line-height:.44rem
      text-align:center
      color:#333
      overflow:hidden
      white-space:nowrap
      text-overflow:ellipsis
</style>