<template>
  <div class="menubar">
      <span class="title">附近商家</span>
      <div class="menu">
        <router-link :to="{ path:'/sellerlist' }" v-for="item in tabs" :key="item">{{item.label}}</router-link>
      </div>
  
  </div>

</template>

<script>

import sellerlist from './NearbySeller/sellerlist.vue'

export default {
  name:'menubar',
  data () {
    return {
        activeName: 'one',
        tabs:[
            {label:'综合排序',name:'one',link:'/sellerlist'},
            {label:'销量高',name:'two',link:'销量高'},
            {label:'速度快',name:'three',link:'速度快'},
            {label:'首单立减',name:'four',link:'首单立减'},
            {label:'筛选',name:'five',link:'筛选'}
        ]
    }
  },
  created () {},
  mounted () {},
  watch: {},
  computed: {},
  methods: {
        handleClick(tab, event) {
      }
  },
  components: {
    sellerlist
  },
}
</script>
<style>
.menubar{
  margin-top: 20px;
    
}

.menubar .title{
    font-size: 16px;
    font-weight: 600;
}

.menubar .menu{
  display: flex;
  display: -webkit-flex;
  justify-content: space-between;
  padding: 10px 0;
  font-size: 14px;

}
</style>