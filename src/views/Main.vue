<template>
  <el-container class="el-container-main">
    <el-header class="el-header">
      <el-row>
        <el-col :span="4">
          <div class="grid-content bg-header"></div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content bg-header"></div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-header"></div>
        </el-col>
      </el-row>
    </el-header>
    <el-header class="el-header-menu">
      <el-menu
        :default-active="activeIndex2"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
        active-text-color="#ffd04b"
      >
        <el-submenu index="1">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-odometer"></i>
            <span slot="title">状态监控</span>
          </template>
          <el-menu-item-group>
            <template slot="title">分组一</template>
            <el-menu-item index="1-1">选项1</el-menu-item>
            <el-menu-item index="1-2">选项2</el-menu-item>
          </el-menu-item-group>
          <el-menu-item-group title="分组2">
            <el-menu-item index="1-3">选项3</el-menu-item>
          </el-menu-item-group>
          <el-submenu index="1-4">
            <template slot="title">选项4</template>
            <el-menu-item index="1-4-1">选项1</el-menu-item>
          </el-submenu>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-setting"></i>
            <span slot="title">系统配置</span>
          </template>
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-key"></i>
            <span slot="title">证书管理</span>
          </template>
        </el-submenu>
        <el-submenu index="4">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-share"></i>
            <span slot="title">SSL配置</span>
          </template>
        </el-submenu>
        <el-submenu index="5">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-s-operation"></i>
            <span slot="title">IPSEC配置</span>
          </template>
        </el-submenu>
        <el-submenu index="6">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-document"></i>
            <span slot="title">日志管理</span>
          </template>
        </el-submenu>
        <el-submenu index="7">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-office-building"></i>
            <span slot="title">单点登录</span>
          </template>
        </el-submenu>
        <el-submenu index="8">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-connection"></i>
            <span slot="title">高可用</span>
          </template>
        </el-submenu>
        <el-submenu index="9">
          <template slot="title">
            <el-divider direction="vertical"></el-divider>
            <i class="el-icon-help"></i>
            <span slot="title">系统维护</span>
          </template>
        </el-submenu>
      </el-menu>
    </el-header>
    <el-main class="el-main">Main</el-main>
    <el-footer class="el-footer">Footer</el-footer>
  </el-container>
</template>
<style>
.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}
.bg-header {
  background: #2962ff;
}

.grid-content {
  border-radius: 0px;
  height: 50px !important;
}
.row-bg {
  padding: 0 0;
  background-color: #f9fafc;
}
.el-container-main {
  height: 100%;
}

.el-menu-vertical-demo {
  display: -webkit-flex;
  height: 40px !important;
}

.el-menu--popup {
  font-size: 10px !important;
  min-width: 150px !important;
  padding: 0 !important;
}

.menu-aside {
  display: -webkit-flex;
}

.el-menu-demo i {
  font-size: 15px !important;
  padding: 0;
}

.el-header {
  padding: 0 !important;
  height: 50px !important;
}

.el-header-menu {
  padding: 0 !important;
  height: 40px !important;
}

.el-footer {
  height: 20px !important;
}
.el-main {
  background-color: #eef5f9;
}
.el-menu-item {
  font-size: 10px !important;
  padding: 0 !important;
  height: 40px !important;
  line-height: 40px !important;
}

.el-submenu {
  padding: 0 !important;
}

.el-divider {
  margin: 0 2px !important;
  height: 40px !important;
}

.el-menu-item-group__title {
  font-size: 10px !important;
}

.el-submenu__title {
  font-size: 10px !important;
  padding: 0 !important;
  height: 40px !important;
  line-height: 40px !important;
}
</style>
<script>
export default {
  data () {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>
