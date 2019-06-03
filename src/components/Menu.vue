<template>
 <div class="menu">
    <el-carousel height="180px" :autoplay="true" arrow="never">
      <el-carousel-item v-for="item in items" :key="item" class="menuPage">
        <div v-for="list in item" :key="list">
            <div class="menu-item">
              <div class="item-img" :style=list.bgcolor>
                <i :class=list.icon></i>
              </div>
              <span class="item-title">{{list.title}}</span>
            </div>
        </div>
        
      </el-carousel-item>
    </el-carousel>
  </div>
</template>

<script>


export default {
  props: {
  },
  data () {
    return {
      items:[
        [
          {title:'美食', bgcolor:'background-color: #fb6c64',icon:'icon-wode iconfont'},
          {title:'超市便利', bgcolor:'background-color: #4eb3f7',icon:'icon-wode iconfont'},
          {title:'素菜水果', bgcolor:'background-color: #8adf3c',icon:'icon-wode iconfont'},
          {title:'美团转送', bgcolor:'background-color: #fcb340',icon:'icon-wode iconfont'},
          {title:'跑腿代购', bgcolor:'background-color: #fc5b63',icon:'icon-wode iconfont'},
          {title:'夜宵', bgcolor:'background-color: #9e79eb',icon:'icon-wode iconfont'},
          {title:'甜点饮品' , bgcolor:'background-color: #fc658e',icon:'icon-wode iconfont'},
          {title:'家常菜', bgcolor:'background-color: #da79ea',icon:'icon-wode iconfont'},
          {title:'龙虾骚烤', bgcolor:'background-color: #4fb5f5',icon:'icon-wode iconfont'},
          {title:'免配送费', bgcolor:'background-color: #c56ddd',icon:'icon-wode iconfont '}
        ],
        [
          {title:'品牌连购', bgcolor:'background-color: #fb6c64',icon:'icon-wode iconfont'},
          {title:'日韩料理', bgcolor:'background-color: #4eb3f7',icon:'icon-wode iconfont'},
          {title:'不辣不欢', bgcolor:'background-color: #8adf3c',icon:'icon-wode iconfont'},
          {title:'浪漫鲜花', bgcolor:'background-color: #fcb340',icon:'icon-wode iconfont'},
          {title:'甜点蛋糕', bgcolor:'background-color: #fc5b63',icon:'icon-wode iconfont'},
          {title:'暖胃粉面', bgcolor:'background-color: #9e79eb',icon:'icon-wode iconfont'},
          {title:'快食简餐', bgcolor:'background-color: #fc658e',icon:'icon-wode iconfont'},
          {title:'送药上门', bgcolor:'background-color: #da79ea',icon:'icon-wode iconfont'},
          {title:'炸鸡零食', bgcolor:'background-color: #4fb5f5',icon:'icon-wode iconfont'},
          {title:'包子粥铺', bgcolor:'background-color: #c56ddd',icon:'icon-wode iconfont'}
        ]
      ]
    }
  },
  created () {},
  mounted () {},
  watch: {},
  computed: {},
  methods: {
    
  },
  components: {},
}
</script>
<style scoped>

.el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__button{
    background-color: #000000!important;
    z-index: 999; 
  }


  .menuPage{
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
      grid-template-rows: auto;
      
  }

  .menu-item{
    display: flex;
    display: -webkit-flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .menu-item .item-img{
    width: 40px;
    height: 40px;
    border-radius: 50%;
    display: flex;
    display: -webkit-flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .menu-item .item-img .iconfont{
    color: white;
    font-size: 20px;
  }

  .menu-item .item-title{
    font-size: 12px;
  }


</style>