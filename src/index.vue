<template>
  <el-menu theme="dark" :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
    <el-menu-item index="1"><router-link to="/">首页</router-link></el-menu-item>
    <el-menu-item index="2"><router-link to="/1">礼包统计管理-赠品</router-link></el-menu-item>
    <el-menu-item index="3"><router-link to="/2">赠品明细</router-link></el-menu-item>
    <el-menu-item index="4"><router-link to="/3">礼包统计管理-优惠券</router-link></el-menu-item>
    <el-menu-item index="5"><router-link to="/4">商户礼包图片</router-link></el-menu-item>
    <el-menu-item index="6"><router-link to="/5">商户赠品图片</router-link></el-menu-item>
  </el-menu>
</template>
<script>
  export default {
    data () {
      return {
        activeIndex: '1'
      }
    },
    methods: {
      handleSelect (key, keyPath) {
        console.log(key, keyPath)
      }
    }
  }
</script>

<style>
.el-menu {
  height: 100%;
  border-radius: 0;
}
.el-menu-item {
  display: block;
  width: 100%;
  text-align: left;
}
.el-menu-item a {
  text-decoration: none;
  display: block;
  font-size: 14px;
}
</style>
