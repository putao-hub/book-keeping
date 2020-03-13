<template>
<div>
<div class="demo-input-suffix">
  
  标题:
  <el-input
  class="input"
    placeholder="请输入内容"
    v-model="input1">
    <i slot="prefix" class="el-input__icon el-icon-search"></i>
  </el-input>
  金额:
  <el-input
  class="input"
    placeholder="请输入金额"
    v-model="input2">
    <i slot="prefix" class="el-input__icon el-icon-search"></i>
  </el-input>
</div>
<el-row class="button">
  <el-button size="medium" round>完成</el-button>
  <el-button class="cancel" size="medium" round>取消</el-button>
 
</el-row>
</div>
</template>

<script>
export default {
  name: "CategoryTable",
  data() {
    return {
      input1: "",
      input2: ""
    };
  }
};
</script>

<style lang="stylus" scoped>
.demo-input-suffix
    padding .2rem
    .input
        margin .3rem 0
.button
    display flex
    justify-content flex-end
    margin-right .2rem
    
        
</style>
