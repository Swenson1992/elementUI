<template>
<div>
  <!-- 头部导航 -->
  <header class="header">
  <el-row>
   <el-col :span="24">
    <el-menu default-active="5" class="el-menu-demo" mode="horizontal" @select="">
    <el-menu-item index="1">高级插件</el-menu-item>
    <el-menu-item index="2">在线商城</el-menu-item>
    <el-menu-item index="3">客户管理</el-menu-item>
    <el-menu-item index="4">系统设置</el-menu-item>
    <el-menu-item index="5">活动发布</el-menu-item>
    </el-menu>
   </el-col>
  </el-row>
  </header>
  <div style="position: relative;height: 60px;width: 100%;"></div>
    <main>
    <div class="main-right">
        <el-table
            :data="tableData3"
            height="750"
            border
            style="width: 80%; float:left">
            <el-table-column
            prop="id"
            label="序号"
            width="180">
            </el-table-column>
            <el-table-column
            prop="name"
            label="款号"
            width="180">
            </el-table-column>
            <el-table-column
            prop="sale1"
            label="采购价">
            </el-table-column>
            <el-table-column
            prop="sale2"
            label="销售价">
            </el-table-column>
            <el-table-column
            prop="sale3"
            label="仓报价">
            </el-table-column>
            <el-table-column
            prop="sale4"
            label="倍率">
            </el-table-column>
        </el-table>
    </div>
    <div class="main-left">
        <el-button>Go!</el-button>
    </div>
    </main>
</div>
</template>


<script>
export default {
  data() {
    let _arr = [];
    for (let index = 1; index <= 200; index++) {
      let _data = {
        id: index,
        name: <el-input />,
        sale1: <el-input />,
        sale2: <el-input />,
        sale3: <el-input />,
        sale4: <el-input />
      };
      _arr.push(_data);
    }
    return {
      tableData3: _arr
    };
  }
};
</script>


<style>
body {
  margin: 0;
}
#app {
  min-width: 1200px;
  margin: 0 auto;
  font-family: "Helvetica Neue", "PingFang SC", Arial, sans-serif;
}
/* 头部导航 */
header {
  z-index: 1000;
  min-width: 1200px;
  transition: all 0.5s ease;
  border-top: solid 4px #3091f2;
  background-color: #fff;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.12), 0 0 6px 0 rgba(0, 0, 0, 0.04);
}
header.header-fixed {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}
header .el-menu-demo {
  padding-left: 300px !important;
}
/* 主内容区 */
main {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  min-width: 1200px;
  min-height: 800px;
  border: solid 40px #e9ecf1;
  background-color: #fcfcfc;
}
main .main-left {
  text-align: center;
  width: 100px;
  float: left;
}
main .main-right {
  -webkit-box-flex: 1;
  -ms-flex: 1;
  flex: 1;
  background-color: #fff;
  padding: 50px 70px;
}
main .el-menu {
  background-color: transparent !important;
}
</style>