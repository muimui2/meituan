<template>
  <div class="adbar">
        <el-card shadow="always" class="cardShop" v-for="shop in shops" :key="shop">

            <div class="shop-img">
                <img :src=shop.shopimg alt="">
            </div>

            <div class="shop-title">
                <div class="shop-logo">
                    <img :src=shop.shoplogo alt="">
                </div>
                <div class="shoptitle">
                    <span class="title">{{shop.title}}</span>
                    <div class="tags">
                        <el-tag class="tag" size="mini" :type=tag.type v-for="tag in tags" :key="tag">{{tag.name}}</el-tag>
                    </div>
                </div>

            </div>

            <div class="shop-slogen">
                {{shop.slogen}}
            </div>

            <div class="shop-list">
                <div class="list-item" v-for="list in shop.items" :key="list">
                    <div class="listimg">
                        <img :src=list.listimg alt="">
                        <div class='listname'>{{list.name}}</div>
                    </div>
                    <span class="item-price">￥{{list.price}}</span>
                </div>

            </div>

        </el-card>
  </div>
</template>




<script>
export default {
  props: {
  },
  data () {
    return {

        tags:[
            {name:'26减3',type:'success'},
            {name:'40减6',type:'warning'},
            {name:'75减12',type:'danger'}

        ],

        shops:[
            {
                shopimg:'https://picsum.photos/400/400.jpg',
                shoplogo:'https://picsum.photos/200/200.jpg',
                title:'木桶饭',
                slogen:'木桶饭蒸出来的米饭香气四溢',
                items: [
                        {listimg:'https://picsum.photos/300/300.jpg',name:'肉香茄子饭',price:'13'},
                        {listimg:'https://picsum.photos/300/300.jpg',name:'香辣土豆丝饭',price:'12'},
                        {listimg:'https://picsum.photos/300/300.jpg',name:'手撕包菜饭',price:'12'}
                ]
            }
        ]
    }
  },
  created () {},
  mounted () {},
  watch: {},
  computed: {},
  methods: {},
  components: {},
}
</script>
<style>

.cardShop{
    display: flex;
    display: -webkit-flex;
    flex-direction: column;
}

.shop-img{
    height: 80px;
    width: 100%;
    overflow: hidden
}

.shop-img img{
    width: 100%;
    
}

.shop-title{
    display: flex;
    display: -webkit-flex;
    align-items: flex-start;
    padding: 0 20px;
    margin-top: -28px;
}

.shop-title .shoptitle{
    margin-left: 10px;
}

.shop-title .shoptitle .title{
    color: white;
    font-size: 16px;
    font-weight: 800px;
    line-height: 18px;
}

.shop-title .shoptitle .tags .tag{
    margin-right: 5px;
}



.shop-title .shop-logo{
    width: 40px;
    height: 40px;
    border-radius: 5px;
    overflow: hidden;
}

.shop-title .shop-logo img {
    width: 100%
}


.shop-list{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 100px;
    grid-gap: 10px;
    padding: 0 10px 20px;
}

.shop-list .list-item .listimg{
    border-radius: 8px;
    overflow: hidden;
    height: 100px;
    position: relative;
}

.shop-list .list-item .item-price{
    color: #F56C6C;
    font-weight: 600;
}

.shop-list .list-item .listimg img{
    width: 100%
}

.shop-list .list-item .listimg .listname{
    position: absolute;
    bottom: 0;
    background-color: black;
    opacity: 0.6;
    right: 0;
    left: 0;
    padding-left: 10px;
    color: white;
    font-size: 12px;

}


.el-card__body{
    padding: 0 0 20px 0;
    border-radius: 10px;
    overflow: hidden;
}

.shop-slogen{
    font-size: 16px;
    padding: 15px 10px;
    font-weight: 600;
}






</style>