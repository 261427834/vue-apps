<template>
  <div class="center">
    <div class="center-wp">
      <!-- 标题 -->
      <el-row>
        <el-col :span="21">
          <div class="plane-title">
            <h3>热门课程</h3>
          </div>
        </el-col>

        <el-col :span="3">
          <div class="right">
            <a href="#">查看更多</a>
          </div>
        </el-col>
      </el-row>

      <!-- 下部 -->
      <!-- 左侧走马灯 -->

      <el-row>
        <el-col :span="6">
          <div class="block centerleft">
            <div class="left-con">
              <div class="left-title">
                <p>热门推荐</p>
                <div class="link-top"></div>
                <p>RENMENTUIJIAN</p>
              </div>
              <el-carousel>
                <el-carousel-item
                  v-for="(item,index) in centerList"  :key="index"  arrow="always"  class="leftlbt" >
                  <p>{{item.class}}</p>
                  <img :src="item.img" />
                </el-carousel-item>
              </el-carousel>
            </div>
          </div>
        </el-col>
        <!-- 中间部分 -->
        <el-col :span="13">
          <div class="plane-content">
            <ul>
              <li v-for="(item,index) in centerList" :key="index" class="center-con left clearfix">
                <div class="li-con">
                  <div class="li-img">
                    <img :src="item.img" />
                  </div>
                  <div class="li-title">
                    <a href="#">{{item.title}}</a>
                  </div>
                  <div class="li-fee">
                    <div class="fee left">{{item.num}}人学习</div>
                    <div class="rmb right">{{item.price}}</div>
                  </div>
                </div>
              </li>
            </ul>
          </div>
        </el-col>
        <!-- 右侧tab -->

        <el-col :span="5">
          <div class="righttab">
            <el-tabs v-model="activeName">
              <el-tab-pane label="热门课程" name="first" class="tabTitle">
                <ul>
                  <li v-for="(item, index) in lessonList" :key="index">
                    <a href>{{item.lesson}}</a>
                  </li>
                </ul>
              </el-tab-pane>
              <el-tab-pane label="热门班级" name="second" class="tabTitle">
                <ul>
                  <li v-for="(item, index) in tabList" :key="index">
                    <a href>{{item.class}}</a>
                  </li>
                </ul>
              </el-tab-pane>
            </el-tabs>
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      centerList: [
        {
          title: "电工",
          price: "免费",
          money: "2000",
          img: require("../assets/电工.jpg"),
          class: "电工(五级)",
          num: 2000
        },

        {
          title: "保安",
          price: "免费",
          money: "2000",
          img: require("../assets/保安.jpg"),
          class: "保安",
          num: 2000
        },
        {
          title: "面点师",
          price: "免费",
          money: "2000",
          img: require("../assets/面点师.png"),
          class: "中式面点师(五级)",
          num: 2000
        },
        {
          title: "楼宇智能管理员",
          price: "免费",
          money: "2000",
          img: require("../assets/楼宇智能管理员.jpg"),
          class: "楼宇智能管理员",
          num: 2000
        },
        {
          title: "钳工",
          price: "免费",
          money: "2000",
          img: require("../assets/钳工.jpg"),
          class: "钳工",
          num: 2000
        }
      ],
      tabList: [
        { class: "中式面点师(五级)" },
        { class: "人力资源管理(五级)" },
        { class: "茶艺师(五级)" }
      ],
      lessonList: [
        { lesson: "中级工商管理(习题精析班)" },
        { lesson: "食品加工与检验" },
        { lesson: "品牌营销VI视觉系统设计" },
        { lesson: "九步玩'赚'微信销售" }
      ],
      activeName: "second"
    };
  }
};
</script>

<style>
.right {
  float: right;
}
.left {
  float: left;
}

.center-wp {
  width: 80%;
  margin: 0px auto;
  background-color: #f5f7fa;
  padding-top: 20px;
}
.plane-title h3 {
  text-align: left;
  font-size: 24px;
  font-weight: normal;
  padding-bottom: 20px;
  height: 24px;
  line-height: 24px;

  color: #333;
}
/* 左侧走马灯 */
.left-con {
  background-color: #ff9684;
  margin: 0 10px;
}
.left-title p {
  color: #fff;
  font-size: 24px;
  text-align: left;
  font-weight: 900;
  padding: 10px;
}
.link-top {
  width: 50%;
  height: 3px;
  border-top: solid #fff 3px;
}

.left-title p:nth-last-child(1) {
  color: #fff;
  font-size: 18px;
  text-align: left;
  font-weight: 300;
  padding: 10px;
}
/* 轮播图 */
.leftlbt {
  display: flex;
  flex-grow: column nowrap;

}

.leftlbt p {
  color: #fff;
  font-size: 20px;
  text-align: center;
 margin:  10px 0;
}
.leftlbt img {
  width: 100%;
  height: auto;
}

/* 中间 */
/* .center-con{
 display: flex;
  flex-grow: row wrap;
} */
.center-con {
  
  margin-right: 10px;
}
.li-con {
  /* width: 220px; */
  background-color: #fff;
}
.li-con .li-title {
  text-align: center;
}
.li-title a {
  font-size: 18px;
}
.li-fee div {
  margin: 10px;
  padding-bottom: 10px;
  border-radius: 10px;
}

.li-fee .rmb {
  color: #3ab57f;
}
.li-img img {
  width: 200px;
  height: inherit;
}

/* 右侧tab */
.righttab {
  height: 430px;
  margin-right: 15px;
  background-color: #fff;
  display: flex;
  justify-content: center;
}

.tabTitle div {
  font-size: 16px;
}
.tabTitle ul li{
list-style: circle;
}
</style>