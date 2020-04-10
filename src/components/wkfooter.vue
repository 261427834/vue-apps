<template>
    <div class="wk-footer">
      <div class="footer-wp">
 <el-row :gutter="20">
   <el-col :span="4">
  <div class="logo"><img :src="linkImg0" alt="logo" /></div>
</el-col>
  <el-col :span="3">
 <div class="footer-title">关于我们</div>
  <div class="footer-text">
     <a href="#">免责声明</a>
   </div>
</el-col>
<el-col :span="3">
  <div class="footer-title">帮助中心</div>
  <div class="footer-text">
    <div><a href="#">会员权益</a></div>
    <div><a href="#">如何观看</a></div>
    <div><a href="#">常见问题</a></div>
  </div>
</el-col>
 <el-col :span="5">
            <div class="footer-title">联系我们</div>
            <div class="footer-text">
             <p>
              <a href="#">客服热线 : 0633-2215282</a>
             </p> 
             <p>
              <a href="#">联系地址 : 日照市东港区人力资源服务产业园12楼</a>
             </p>
              
            </div>
</el-col>
<el-col :span="3">
              <div class="footer-title">商务合作</div>
              <div class="footer-text">
                <p> <a href="#">渠道加盟</a></p>
               <p> <a href="#">讲师合作</a></p>
               
              </div>
</el-col>
 <el-col :span="2" class="">
      <div class="code-img right">
         <img :src="linkImg1" alt="二维码"  />
       
        
       </div>
             
   </el-col>
   <el-col :span="2" class="">
      <div class="code-img right">
        
       
         <img :src="linkImg2" lt="二维码" />

       </div>
             
   </el-col>

        </el-row>





        <el-row>
          <el-col :span="24">
            <div class="footer-down">
              <div class="text">
                Copyright2020© 据家微课.
                日照市东港区杰出培训学校保留所有权利&nbsp;|&nbsp;
                沪ICP备20003109号-1
              </div>
            </div>
          </el-col>
        </el-row>



      </div>
    </div>
</template>

<script>
export default {
data(){
  return{
    linkImg0:require("../assets/footer-logo.png"),
    linkImg1:require("../assets/wx_fot_wxapp.jpg"),
    linkImg2:require("../assets/code.jpeg"),
    
  }
}
}
</script>

<style scoped>


/* footer */
.wk-footer{
  margin-top: 50px;
    width: 100%;
    /* height: 300px; */
    background-color: #112641;
    padding-top: 50px;

}
.footer-wp{
  width: 80%;
  margin: 0 auto;
  height: 300px;
  
}


.footer-text a , .footer-text p a{
  color: #fff;
  text-align: left;
}

.footer-title {

  font-size: 20px;
    font-weight: 400;
    color: #fff;
    line-height: 80px;
 
  text-align: left;
}
.code-img img{
  width: 100px;
}
.footer-down{
  color: #999999;
    font-size: 13px;
    text-align: center;
    margin-top: 30px;
}
</style>