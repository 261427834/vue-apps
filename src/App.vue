<template>
  <div id="app">
    <top></top>

    <cover></cover>

    <center></center>
    <center></center>
    <center></center>
    <center></center>
    <teacher></teacher>
    <news></news>

    <wkfooter></wkfooter>
  </div>
</template>

<script>
import top from "./components/top.vue";
import cover from "./components/cover.vue";

import center from "./components/center.vue";
import teacher from "./components/teacher.vue";
import wkfooter from "./components/wkfooter.vue";
import news from "./components/news.vue";

export default {
  name: "App",
  components: {
    top,
    cover,
    wkfooter,
    teacher,
    news,
    center
    // scrollTop
  }
};
</script>

<style>
/* 总体设定 */

.left {
  float: left;
}
.right {
  float: right;
}
.clearfix {
  overflow: auto;
  zoom: 1;
}
a {
  font-size: 15px;
  font-weight: 400;
  color: #555;
  line-height: 25px;
  text-align: left;
}
</style>
