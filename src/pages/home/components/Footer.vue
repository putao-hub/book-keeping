<template>
  <div class="footer">
    <div class="footer-left">
      <span class="footer-icon iconfont">&#xe62b;</span>
      <p class="footer-text">明细</p>
    </div>
    <router-link to="/category">
      <div class="footer-edit">
        <span class="footer-icon iconfont">&#xe617;</span>
        <p class="footer-text">记账</p>
      </div>
    </router-link>
    <div class="footer-right"> 
      <span class="footer-icon iconfont">&#xe743;</span>
      <p class="footer-text">图表</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeFooter"
};
</script>

<style lang="stylus" scoped>
.footer
    position absolute
    overflow hidden
    bottom 0
    left 0
    right 0
    background #2a9ff6
    height 1.27rem
    display flex
    justify-content space-around
    color #fff
    padding-top .1rem
   
    box-sizing border-box
    .footer-edit
        color #fff
    .footer-text
        padding-top .2rem
    .footer-icon
        padding-left .05rem
        font-size .45rem
</style>
