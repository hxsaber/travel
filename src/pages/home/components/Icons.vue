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
    data () {
        return {
            iconList:[{
                id:'0001',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:'景点门票'
            },{
                id:'0002',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
                desc:'一日游'
            },{
                id:'0003',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
                desc:'成都必游'
            },{
                id:'0004',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png",
                desc:'川剧变脸'
            },{
                id:'0005',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/b6/aae239efe3496602.png",
                desc:'成都火锅'
            },{
                id:'0006',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/b8/c5dcdb58deec2402.png",
                desc:'碧峰峡'
            },{
                id:'0007',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png",
                desc:'游乐场'
            },{
                id:'0008',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png",
                desc:'熊猫基地'
            },{
                id:'0009',
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
                desc:'动植物园'
            }],
            swiperOption:{
                autoplay:false
            }
        }
    },
    computed:{
        pages () {
            const pages = []
            this.iconList.forEach((item,index) => {
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