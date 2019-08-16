<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">  
                    <img class="item-img" :src="item.imgUrl">
                </div>    
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
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
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },{
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },{
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },{
            id:'0004',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
            title:'谭鸭血老火锅',
            desc:"麻辣又好吃"
        },]
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
.item-img-wrapper    
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
        width: 100%
.item-info
    padding: .1rem
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

</style>
