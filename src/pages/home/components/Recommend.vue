<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img :src="item.imgUrl" class="item-img">
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'HomeRecommend',
    data () {
        return {
            recommendList:[{
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1905/32/32ad7003179269d2a3.img.jpg_200x200_aee761e4.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },{
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1905/32/32ad7003179269d2a3.img.jpg_200x200_aee761e4.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },{
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1905/32/32ad7003179269d2a3.img.jpg_200x200_aee761e4.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },{
            id:'0004',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1905/32/32ad7003179269d2a3.img.jpg_200x200_aee761e4.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        }]
        }
    }
}
</script>

<style lang="stylus" scoped>
.title  
    margin-top: .2rem
    line-height: .8rem    
    color: #212121    
    background: #eee
    text-indent: .2rem
.item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
        width: 1.7rem
        height: 1.7rem
        padding: .1rem
    .item-info
        flex: 1
        padding: .1rem
        min-width: 0
        .item-title
            line-height: .54rem
            font-size: .32rem
            overflow: hidden
            white-space: nowrap
            text-overflow: ellipsis
        .item-desc    
            line-height: .4rem
            color: #ccc
            overflow: hidden
            white-space: nowrap
            text-overflow: ellipsis 
        .item-button
            line-height: .36rem
            margin-top: .16rem
            background: #ff9300
            padding: .05rem .2rem
            border-radius: .06rem
            color: #fff
</style>
