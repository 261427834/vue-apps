<template>
  <div class="navbar">
    <el-row>
      <el-col :span="3">
        <el-menu
          :default-active="activeIndex"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#3c81f9"
          text-color="#fff"
          active-text-color="#fff"
          
        >

          <el-submenu index="2">
            <template slot="title">导航菜单</template>
         
            <el-submenu index="2-4">
              <template slot="title">职业证书</template>
              <el-menu-item index="2-4-1">财会经济</el-menu-item>
              <el-menu-item index="2-4-2">建筑工程</el-menu-item>
              <el-menu-item index="2-4-3">消防安全</el-menu-item>
            </el-submenu>
          </el-submenu>
        </el-menu>
      </el-col>

      <el-col :span="21" class="navbar2">
        <el-menu
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#fff"
          text-color="#000"
          active-text-color="#fff"
        >
          <el-menu-item index="2">
            <a href="#" target="_blank">首页</a>
          </el-menu-item>
          <el-menu-item index="3">
            <a href="#" target="_blank">发现课程</a>
          </el-menu-item>
          <el-menu-item index="4">
            <a href="#" target="_blank">公开课直播</a>
          </el-menu-item>
          <el-menu-item index="5">
            <a href="#" target="_blank">面授课程</a>
          </el-menu-item>
           <el-menu-item index="6">
            <a href="#" target="_blank">企业商学院</a>
          </el-menu-item>
          <el-menu-item index="7">
            <a href="#" target="_blank">灵活就业</a>
          </el-menu-item>
          <el-menu-item index="8">
            <a href="#" target="_blank">关于我们</a>
          </el-menu-item>
        </el-menu>
      </el-col>
    </el-row>
  </div>
</template>


<script>
export default {
  name: "navbar",
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

<style>

*{
    padding: 0;
    margin: 0;
    border: 0;
}
.navbar2 li{
    height: 50px;
}
.navbar2 a{

    display: block;
    text-align: center;
    color: #333;
    font-size: 16px;
    line-height: 50px;

}
</style>