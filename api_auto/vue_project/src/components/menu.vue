<template>
  <div>
    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      :default-openeds = "['1', '2']"
      @close="handleClose">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-star-off"></i>
          <span>功能区</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="1-1">项目管理</el-menu-item>
          <el-menu-item index="1-2">环境管理</el-menu-item>
          <el-menu-item index="1-3">接口库</el-menu-item>
          <el-menu-item index="1-4">线上监控</el-menu-item>
          <el-menu-item index="1-5">接口文档</el-menu-item>
          <el-menu-item index="1-6">Postman</el-menu-item>
          <el-menu-item index="1-7">在线抓包</el-menu-item>
          <el-menu-item index="1-8">其他</el-menu-item>
        </el-menu-item-group>
      </el-submenu>

      <el-submenu index="2">
        <template slot="title">
          <i class="el-icon-s-custom"></i>
          <span>用户区</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="2-1">个人资料</el-menu-item>
          <el-menu-item index="2-2">个人贡献</el-menu-item>
          <el-menu-item index="2-3">发送消息</el-menu-item>
          <el-menu-item index="2-4">推出</el-menu-item>
        </el-menu-item-group>
      </el-submenu>

      <el-submenu index="3">
        <template slot="title">
          <i class="el-icon-setting"></i>
          <span>维护区</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="3-1">后台管理</el-menu-item>
          <el-menu-item index="3-2">用户管理</el-menu-item>
          <el-menu-item index="3-3">查看日志</el-menu-item>
          <el-menu-item index="3-4">发布公告</el-menu-item>
          <el-menu-item index="3-5">权限管理</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: "Menu",
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style scoped>

</style>
