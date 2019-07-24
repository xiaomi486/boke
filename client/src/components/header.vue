<template>
  <div class="header">
    <header>
      <div class="logo">
        <img src="/img/logo.png" alt />
      </div>
      <div class="login">
        <el-button type="primary">登陆</el-button>
        <el-button>注册</el-button>
      </div>
       <div class="nav">
        <el-tabs v-model="activeName" @tab-click="handleClick">
          <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
          <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
        </el-tabs>
      </div>
    </header>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  data() {
    return {
      activeName: "second"
    };
  },
  methods: {
    handleClick(tab: any, event: any) {
      console.log(tab, event);
    }
  }
});
</script>
<style lang="less" scoped>
.header{
    height: 67px;
    .logo{
      width: 300px;
      height: 67px;
      float: left;
      img{
        height: 100%;
        width: 100%;
      }
    }
    .nav{
      float: right;
    }
    .login{
      float: right;
    }
}
</style>
