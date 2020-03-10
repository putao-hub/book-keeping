<template>
  <div>
    <div class="header">
      <div class="header-title">
        <span class="header-icon iconfont">&#xe631;</span>
        <p class="header-text">极简记账</p>
      </div>
      <div class="header-content">
          <div class="header-content-title">
              <p class="text">日期</p>
              <p class="text">收入</p>
              <p class="text">支出</p>
          </div>
          <div class="header-content-number">
              <div class="number">
                  <div class="block">
                    <el-date-picker
                    v-model="value2"
                    type="month"
                    placeholder="选择月">
                    </el-date-picker>
                </div>
              </div>
              <p class="number">0.00</p>
              <p class="number">0.00</p>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader",
   data() {
      return {
       
        value2: '',
     
      };
    }
};
</script>

<style lang="stylus" scoped>
>>> .el-input__inner
    height .44rem
    line-height .44rem
    width 40%
    padding-right 0
   
   >>>.el-input__icon
        height .44rem
        line-height .44rem

.header
    width 100%
    height 2.54rem
    background #2a9ff6
    color #fff
    overflow hidden
    padding-left .1rem
    .header-title
        height 50%
        position relative
        .header-text
            line-height 1.27rem
            text-align center
            font-size .4rem
        .header-icon
            position absolute
            top .35rem
        .iconfont
            font-size .54rem
           
    .header-content
        padding-top .3rem
        height 50%
       
        .header-content-title
            display flex
            .text
                flex 1
        .header-content-number
            display flex
            padding-top .2rem
            .number
                flex 1
                overflow hidden
               
        
</style>
