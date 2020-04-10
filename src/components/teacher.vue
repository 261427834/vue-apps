<template>
          <!-- 教师 -->
        <div class="main-teacher">
          <div class="main-teacher-title">
            <h3>讲师风采</h3>
          </div>
          <div class="main-teacher-con">
            <ul class="item">
              <!-- 4个教师 -->
              <li v-for="(item,index) in teacherlist" :key="index">
                <img :src="item.img" alt="老师头像" />
                <h3>{{item.name}}</h3>
                <h5>{{item.title}}</h5>
                <span>{{item.skill}}
                </span>
              </li>
              <!-- <li>
                <img src="img/teacher2.png" alt="老师头像" />
                <h3>老师姓名</h3>
                <h5>老师头衔</h5>
                <span>销售团队激励，团队凝聚力打造，
                  销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导
                </span>
              </li>
              <li>
                <img src="img/teacher3.png" alt="老师头像" />
                <h3>老师姓名</h3>
                <h5>老师头衔</h5>
                <span>销售团队激励，团队凝聚力打造，
                  销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导
                </span>
              </li>
              <li>
                <img src="img/teacher4.png" alt="老师头像" />
                <h3>老师姓名</h3>
                <h5>老师头衔</h5>
                <span>销售团队激励，团队凝聚力打造，
                  销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导
                </span>
              </li> -->
            </ul>
          </div>
        </div>
</template>

<script>
export default {
data(){
  return {
    teacherlist:[
{name:'老师姓名',
skill:'销售团队激励，团队凝销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导',
title:'老师头衔',
img:require('../assets/teacher1.png')
},
{name:'老师姓名',
skill:'销售团队激励，团队凝销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导',
title:'老师头衔',
img:require('../assets/teacher2.png')
},
{name:'老师姓名',
skill:'销售团队激励，团队凝销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导',
title:'老师头衔',
img:require('../assets/teacher3.png')
},
{name:'老师姓名',
skill:'销售团队激励，团队凝销售技巧，职业素养提升,职业生涯规划，员工心理健康疏导',
title:'老师头衔',
img:require('../assets/teacher4.png')
},

    ]
  }
}
}
</script>

<style  scoped>

/* <!-- 教师 --> */
.main-teacher{
  width: 80%;
margin: 0 auto;

background-color: #f5f7fa;
}
.main-teacher-title h3 {
text-align: left;
font-size: 24px;
font-weight: normal;
padding-bottom: 20px;
height: 24px;
line-height: 24px;

color: #333;
}
.main-teacher-con .item{
  display: flex;
flex-grow: row nowrap;
justify-content: space-around;

}
.main-teacher-con li{
  width: 210px;

}


.main-teacher-con li img{
  width: 170px;
  height: 200px;
  margin-bottom: 10px;

}
.main-teacher-con li h3{
  font-size: 18px;
    font-weight: 500;
    color: #333;
    line-height: 26px;

}
.main-teacher-con li h5{
  font-size: 14px;
  font-weight: 400;
  color: #999999;
  line-height: 28px;
}
.main-teacher-con .item span {
  font-size: 9px;
    font-weight: 400;
    margin-top: 5px;
    color: #666;
    line-height: 16px;
    text-align:left;

    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px
}
</style>