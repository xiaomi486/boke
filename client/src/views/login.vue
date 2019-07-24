<template>
<div class="login">
<el-card class="box-card">
  <div slot="header" class="clearfix">
    <span>卡片名称</span>
  </div>
    <el-form ref="form" :model="form" label-width="80px">
  <el-form-item label="账号">
    <el-input v-model="form.username"></el-input>
  </el-form-item>
  <el-form-item label="密码">
    <el-input v-model="form.password"></el-input>
  </el-form-item>
    <el-checkbox v-model="checked">记住密码</el-checkbox>
   <el-form-item>
         <el-button type="primary">登陆</el-button>
  </el-form-item>
</el-form>
</el-card>
  
</div>
    
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    data() {
      return {
        form: {
          username: '',
          password: '',
        },
        checked:true
      }
    },
})
</script>
<style lang="less" scoped>
    .login{
        height: 300px;
        width: 460px;
        margin: 200px auto;
        border-radius: 5px;
    }
</style>
