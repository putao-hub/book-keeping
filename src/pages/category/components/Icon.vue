<template>
  <div>
    <div class="header">
      <div class="outcome" @click="cur = 0" >
         支出
     
       
      </div>
      <div class="income" @click="cur = 1">
       收入 
      </div>
      <router-link to="/">
        <div class="back">取消</div>
      </router-link>
      
    </div>

    <div v-show="cur == 0" >
      <div class="icons">
        <div class="icon" v-for="item of outcomeList" :key="item.id"
        
        >
          <div class="icon-img">
            <!-- iconfont  icon-img-content {{item.icon}} -->
            <!-- <i :class="['{iconfont icon-img-content},{{item.icon}}']"></i> -->
            <!-- 动态类名和静态类名一起绑定 -->
            <i :class="['iconfont', 'icon-img-content', item.icon,{active:active == item.id}]"   @click = selected(item.id) ></i>
          </div>
          <p class="icon-dec">{{ item.dec }}</p>

        </div>
      </div>
    </div>
    <div v-show="cur == 1">
      <div class="icons">
        <div class="icon" v-for="item of incomeList" :key="item.id"
          @click = selected(item.id)
          :class="{active:active == item.id}"
        >
          <div class="icon-img">
             <i :class="['iconfont', 'icon-img-content', item.icon,{active:active == item.id}]"   @click = selected(item.id) ></i>
          </div>
          <p class="icon-dec">{{ item.dec }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CategoryIcon",
  data() {
    return {
      cur: 0,
    
      
      outcomeList: [
        {
          id: "001",

          dec: "餐饮",
          icon: "iconcanyin"
        },
        {
          id: "002",
          icon: "iconshuiguo",
          dec: "水果"
        },
        {
          id: "003",
          icon: "iconriyongpin",
          dec: "日用品"
        },
        {
          id: "004",
          icon: "iconlingshi",
          dec: "零食"
        },
        {
          id: "005",
          icon: "iconjiaotong",
          dec: "交通"
        },
        {
          id: "006",
          icon: "iconyouxi",
          dec: "游戏"
        },
        {
          id: "007",
          icon: "iconshumachanpin",
          dec: "数码产品"
        },
        {
          id: "008",
          icon: "iconqian",
          dec: "还款"
        }
      ],
      incomeList:[
        {
          id: "001",

          dec: "礼金",
          icon: "iconlijin"
        },
        {
          id: "002",

          dec: "理财",
          icon: "iconlicai"
        },
         {
          id: "003",

          dec: "兼职",
          icon: "iconxiaoxijianzhi"
        },
        {
          id: "004",

          dec: "工资",
          icon: "iconlicai"
        },
      ],
      active:'001',
    


    };
  },
  methods:{
    selected(id){
      this.active = id
      
      
    },
  
    
   
  },
  
}
</script>

<style lang="stylus" scoped>

.header
    width 100%
    height 1.2rem
    background #2a9ff6
    color #fff
    overflow hidden
    position relative
    .outcome
        float left
        padding-left 35%
        padding-top 8%
        font-size .34rem
    .income
        float right
        padding-right 35%
        padding-top 8%
        font-size .34rem
    .back
        position absolute
        right .2rem
        bottom .3rem
        color #fff
.icons
      overflow: hidden
      height: 0
      padding-bottom:83%
      padding-top .2rem
      .icon
          position :relative
          height:0
          float: left
          width:25%
          padding-bottom :25%
          .icon-img
              position :absolute
              bottom :.55rem
              top:0
              left:0
              right:0
              .iconfont
                  font-size 1.06rem
                  position absolute
                  left 50%
                  top 50%
                  transform translate(-50%, -50%)
                  color #ccc
          .icon-dec
              position :absolute
              bottom :0
              left:0
              right:0
              color:#000
              height:.55rem
              line-height:.55rem
              text-align:center
          .active
              background #2a9ff6
              border-radius .54rem
         
          
</style>
