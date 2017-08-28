<template>
  <el-menu theme="dark" :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
    <el-menu-item :index="item.index" v-for="(item, index) in menuData"><router-link :to="item.url">{{item.name}}</router-link></el-menu-item>
  </el-menu>
</template>
<script>
  export default {
    data () {
      return {
        activeIndex: '1'
      }
    },
    props:['menuData'],
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
