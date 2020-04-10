<template>
      <!-- news -->
    <div class="news">
      <div class="news-wp">
        <div class="news-title-wp">
          <div class="news-title left">最新新闻</div>
          <div class="news-more right">
            <a href="#">查看更多</a>
          </div>
        </div>
        <div class="news-item-wp ">
          <!-- 新闻6个 item -->
          <ul>
            <el-row>
              <el-col :span="12" v-for='(item,index) in newslist' :key='index'>
                <li class="news-item">
                  <el-row>
                    <el-col :span="6">
                      <div class="news-item-pic">
                        <img :src="item.src" alt="新闻图片" />
                      </div>
                    </el-col>
                    <el-col :span="14">
                      <h3>{{item.title}}</h3>
                      <p>{{item.text}}</p>
                      <el-row>
                        <el-col :span="4" class="right">
                          <span>time</span>
                        </el-col>
                      </el-row>
                    </el-col>
                  </el-row>
                </li>
              </el-col>
            </el-row>


          </ul>
        </div>
      </div>
    </div>
</template>

<script>
export default {


    data(){
        return{
// news 数据循环
      newslist: [
        {
            src:require('../assets/newspci1.png'),
          title: '我校园内设的专业及院校科查看方式有哪些，入学须知',
          text: '大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二维码、APP,录取通知书越来越“潮范儿”了 大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二'
      
        },
        {
         src:require('../assets/newspci2.png'),
          title: '我校园内设的专业及院校科查看方式有哪些，入学须知',
          text: '大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二维码、APP,录取通知书越来越“潮范儿”了 大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二'
        },
        {
          src:require('../assets/newspci3.png'),
          title: '我校园内设的专业及院校科查看方式有哪些，入学须知',
          text: '大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二维码、APP,录取通知书越来越“潮范儿”了 大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二'
        },
        {
         src:require('../assets/newspci4.png'),
          title: '我校园内设的专业及院校科查看方式有哪些，入学须知',
          text: '大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二维码、APP,录取通知书越来越“潮范儿”了 大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二'
        },
        {
         src:require('../assets/newspci1.png'),
          title: '我校园内设的专业及院校科查看方式有哪些，入学须知',
          text: '大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二维码、APP,录取通知书越来越“潮范儿”了 大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二'
        },
        {
          src:require('../assets/newspci1.png'),
          title: '我校园内设的专业及院校科查看方式有哪些，入学须知',
          text: '大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二维码、APP,录取通知书越来越“潮范儿”了 大学录取通知书即普通高等院校给录取者发放的入学凭证。随着时代的发展,从纸质、毛笔手写到二'
        },
      ],
        }
    }

}
</script>

<style>
/* <!-- news --> */
.news-wp{
  width: 80%;
  margin: 0 auto;
  
  background-color: #f5f7fa;
padding-top: 40px;
}
.news-title {
  text-align: left;
  font-size: 24px;
  font-weight: normal;
  padding-bottom: 20px;
  height: 24px;
  line-height: 24px;
  
  color: #333;
}
.news-wp::after{
  content: "";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}
.news-title-wp::after{
  content: "";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}

/* news-item */

.news h3{
  font-size: 15px;
    font-weight: 400;
    color: #555;
    line-height: 25px;
    text-align: left;
}
.news a{
  font-size: 15px;
  font-weight: 400;
  color: #555;
  line-height: 25px;
  text-align: left;
}

 .news span {
  font-size: 9px;

}
.news p{
  font-size: 9px;
  font-weight: 400;
  color: #999;
  line-height: 15px;
  text-align: left;
}
.news-item-pic img {
  width: 100px;
}
</style>