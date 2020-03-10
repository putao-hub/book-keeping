<template>
  <div class="list">
    <div class="list-title ">
      <div class="list-title-date">
          <span class="date-text">17</span>
            日/周五
      </div>
     
     
        <div class="list-title-price ">
            <span class="income-color"> 收</span> 200.00 &nbsp;&nbsp;
            <span class = "outcome-color"> 支</span> 500.00
        </div>
     
    </div>
    <div class="list-content border-bottom">
      <div class="list-content-icon">
        <div class="iconfont back-icon">&#xe611;</div>
      </div>
      <div class="list-content-text">
        红包
      </div>
      <div class="list-content-price">
        200.00
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "PriceList",
  data() {
    return {
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1518 弄"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
.list
    position :absolute
    overflow :hidden
    top:2.58rem
    left:0
    right :0
    bottom :0
.list-title
    overflow hidden
    height .86rem
    line-height: .86rem
    .list-title-date
        padding-left .1rem
        float:left
        .date-text
            font-size .4rem
    .list-title-price
        min-width:1.04rem
        padding  0 .1rem
        float right
        text-align center 
        .income-color
            color red
        .outcome-color
            color blue  
         
.list-content
    line-height: .86rem
    display:flex
    color:#000
    .list-content-icon
        width 0.6rem
        float:left
        .back-icon
            text-align :center
            font-size :.45rem
            padding-left .2rem
            color #2a9ff6
    .list-content-text
        flex:1
        line-height:.62rem
        margin-top:.12rem
        margin-left :.2rem
        border-radius : .12rem
        height :.62rem
        padding-left :.2rem
    .list-content-price
        min-width:1.04rem
        padding : 0 .1rem
        float:right
        text-align :center
    
</style>
