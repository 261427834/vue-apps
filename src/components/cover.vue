<template>
  <div class="cover">
       <el-carousel indicator-position="outside">
    <el-carousel-item v-for="(item,index) in coverlist" :key="index">
     <img   :src="item.img" alt="cover"  />
    </el-carousel-item>
  </el-carousel>
  </div>
</template>

<script>
export default {
data(){
    return{
coverlist:[{

img:require('../assets/maincover.png'),
img:require('../assets/maincover.png'),

}


]
    }
}
}
</script>

<style>
.cover{
  width: 100%;
  /* height: 410px; */
}
 .cover img{
  
     /*设置图片宽度和浏览器宽度一致*/
      /* height:100%; */
       width: 100%;
    
    
 }
</style>