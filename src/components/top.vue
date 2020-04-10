<template>
      <!-- 顶部 -->
    <div class="wk-top-nav">
      <div class="top-bar">
        <div class="top-bar-wp">
          <div class="top-bar-left left">
            <ul>
              <li>
                <span><a href="#">据家商城</a></span>
              </li>
              <li>
                <span><a href="#">据家商城</a></span>
              </li>
              <li>
                <span><a href="#">据家商城</a></span>
              </li>
              <li>
                <span><a href="#">据家商城</a></span>
              </li>
              <li>
                <span><a href="#">据家商城</a></span>
              </li>
            </ul>
          </div>
          <div class="top-bar-right right">
            <ul>
              <li>
                <span><a href="#">开通会员</a></span>
              </li>
              <li>
                <span><a href="#">推荐好友</a></span>
              </li>
              <li>
                <span><a href="#">商务合作</a></span>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <!-- 导航 -->
      <div class="top-main ">
        <!-- s上部 -->
        <div class="search-section">
          <!-- logo -->
          <div class="top-logo">
            <img :src="linkImg" alt="logo" />
          </div>
          <div class="top-search">
            <div class="input-search">
              <div class="input-wp">
                <el-input
    placeholder="请输入内容"
    v-model="topInput">
    <i slot="suffix" class="el-input__icon el-icon-search"></i>
  </el-input>
              </div>
              <!-- 面包屑导航 -->
              <div class="search-tags">
                <ul>
                  <li>
                    <span><a href="#">雅思</a></span>
                  </li>
                  <li>
                    <span><a href="#">雅思</a></span>
                  </li>
                  <li>
                    <span><a href="#">雅思</a></span>
                  </li>
                  <li>
                    <span><a href="#">雅思</a></span>
                  </li>
                  <li>
                    <span><a href="#">雅思</a></span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="top-user">
            <div class="use-main">
              <ul>
                <li>
                  <a href="#">我的学习</a>
                </li>
                <li>
                  <a href="#">我的工作</a>
                </li>
                <li>
                  <a href="#">我的考试</a>
                </li>
              </ul>
            </div>
            <div class="sign-in">
              <a href="#">登录</a>
            </div>
            <div class="user-icon">
              <img :src="linkImg2" alt="用户头像">
            </div>
          </div>
        </div>
         <navbar></navbar>
    
      </div>
      <!-- 遮罩 -->
      <div class="cover"></div>
    </div>
</template>

<script>
import navbar from './navbar.vue'
export default {
 name:'top',
   components:{
navbar,
   },


data(){
 
  return{
    linkImg:require('../assets/top-logo.png'),
    linkImg2:require('../assets/user-icon.jpg'),
    topInput:"",
  }
}
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  /* box-sizing: border-box; */
  list-style: none;
  /* text-align: center; */
  text-decoration: none;
  
}
/* top 导航 */
.top-bar {
  width: 100%;
}
.top-bar-wp a:last-child {
  color: #787c82;
  padding: 0 20px;
  border-right: 1px solid #787c82;
  font-size: 13px;
}

.top-bar-wp {
  width: 80%;
  height: 30px;
  margin: 0 auto;
  background-color: #f5f7fa;
}
.top-bar-right li,
.top-bar-left li {
  display: inline-block;
  line-height: 30px;
}
/* 导航 */
.top-main {
  width: 70%;
  margin: 0 auto;
  padding-top: 20px;
}
/* 导航上部 */
.search-section {
  display: flex;
  width: 100%;
  justify-content: space-between;
}
/* logo */
.top-logo {
  width: 230px;
  text-align: left;
}
/* top-search */
.top-search {
  width: 400px;
  margin-left: 50px;
}
.input-search input {
  width: 400px;
  height: 40px;
  text-align: left;
}

/* 面包屑导航 */
.search-tags ul {
  display: flex;
  flex-grow: column nowrap;
}
.search-tags span {
  margin-right: 10px;
}
.search-tags span a {
  color: #787c82;
  font-size: 9pt;
  line-height: 33px;
}
/* top-user */
.top-user {
  display: flex;

  height: 40px;
  line-height: 40px;

  padding-right: 30px;
}
.use-main ul {
  display: flex;
}
.use-main ul li {
  margin: 0 15px;
  align-items: center;
  flex-basis: 60px;
}
.top-user .use-main ul a {
  font-size: 14px;
  color: #606367;
  
}
.user-icon img {
  width: 30px;
  height: 30px;
}
/* 导航下部 */
.main-nav {
  display: flex;
}
/* 前方导航条 */
.tab-nav {
    width: 230px;
    
}
.tab-nav li {
  height: 50px;
  line-height: 50px;
  position: relative;
  padding: 0 15px;
  background: #3c81f9;
  box-sizing: border-box;
}
.tab-nav li a {
  display: block;
  width: 100%;
  height: 100%;
  color: white;
  line-height: 50px;
  text-align: left;
}

/* 后方主导航条 */
.drop-nav li {
  float: left;
  height: 50px;
  line-height: 50px;
  position: relative;
  width: 119px;
}
.drop-nav li a {
  width: 120px;
  display: block;
  text-align: center;
  color: #333;
  font-size: 16px;
}
</style>