<template>
  <div class="headerbar">

        <el-link type="info" :underline="false">
           <i class="iconfont icon-ziyuan"></i>
          {{address}}
           <i class="iconfont icon-right"></i>
        </el-link>
        <el-input :placeholder=input class="search-input"></el-input>

  </div>
</template>

<script>
export default {
  props: {
  },
  data () {
    return {
        input:'哈佬鸡 满30减20',
        address :"东方骏园",
        redbag : "https://picsum.photos/400/400.jpg"
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


.search-input{
  margin-top: 10px;
}

.icon-ziyuan{
  color: #ffc107;
}

.search-input .el-input__inner{
  border-radius: 10px;
}

.iconfont.icon-right{
  font-size: 10px;
}


</style>