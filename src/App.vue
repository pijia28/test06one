<template>
  <div id="app">
     <div class="header">
      <div class="header-up">
      <img src="@/assets/redflag.png" alt="" style="height:100%">
      <div class="search">
          <div class="search-in">
            <input type="text" style="height:30px;width:200px;">
            <button style="height:30px;">查询</button>
          </div>
      </div>   
      </div>
      <div class="header-bottom">
        <div class="navi-item">网站首页</div>
        <div class="navi-item">品牌空间</div>
        <div class="navi-item">全线车系</div>
        <div class="navi-item">企业信息</div>
        <div class="navi-item">预约试驾</div>
        <div class="navi-item">经销商查询</div>
        <div class="navi-item">专家答疑</div>
        <div class="navi-item">红旗服务</div>
      </div>
      </div>
     <div class="center">
       <div class="center-navi">
        <div class="center-navi-title">车型分类</div>
        <div class="center-navi-item" @click="showcar('H5')">红旗H5</div>
        <div class="center-navi-item" @click="showcar('H7')">红旗H7</div>
        <div class="center-navi-item" @click="showcar('L7')">红旗L7</div>
        <div class="center-navi-item" @click="showcar('L9')">红旗L9</div>
        <!-- <div class="center-navi-item">红旗LS5</div>
        <div class="center-navi-item">红旗H5</div> -->
       </div>
     <div class="center-biging">
        <img :src="require('@/assets/'+currentcar+currentBig+'.jpg')" alt="" class="big-img">
     </div>
     <div class="center-smalling">
       <img @click="changeBig('1')" class="small-img" :src="require('@/assets/'+currentcar+'1.jpg')" alt="picture1">
       <img @click="changeBig('2')" class="small-img" :src="require('@/assets/'+currentcar+'2.jpg')" alt="picture2">
       <img @click="changeBig('3')" class="small-img" :src="require('@/assets/'+currentcar+'3.jpg')" alt="picture3">
       <img @click="changeBig('4')" class="small-img" :src="require('@/assets/'+currentcar+'4.jpg')" alt="picture4">
     </div>
    </div>
     <div class="footer"><span><a href="#">网站地图</a>&nbsp;|&nbsp;<a href="#">购车计算器</a>&nbsp;|&nbsp;<a href="#">免责声明</a>&nbsp;|&nbsp;<a href="#">联系红旗</a></span>
       <span>版权所有******copyright@2015</span>   
      </div>
  </div>
</template>
<script>
export default {
    data(){
      return{
         currentcar:"H5" ,
         currentBig:"1",
        /*  currentBig:k,  */
      }
    },
   methods:{
     showcar(x){
      this.currentcar=x;
     },
      changeBig(k){
       this.currentBig=k;
     } 
   },
}
</script>
<style>
 a{
  color:white;
  text-decoration:none;
  font-weight:bold;
 }
 #app {
   width:100%;
   height:100%;
   left:0px;
   top:0px;
  /*  background-color:rgb(30, 218, 30); */
   position:absolute;
} 
.big-img{
  width:95%;
  height:100%;
}
.small-img{
  width:81%;
  height:23%;
  border-color: royalblue;
}
.header{
  width:100%;
  height:15%;
  /* background-color:pink; */
}
.center{
  width:100%;
  height:78%;
  display:flex;
  align-items:center;
/*   background-color:greenyellow; */
}
.center-navi{
  height:90%;
  width:15%;
 /*  background-color:rosybrown; */
}
.center-navi-title{
  width:80%;
  height:8%;
 /*  background-color: pink; */
  border-bottom-style:solid;
  border-bottom-color:red;
  display:flex;
  align-items:flex-end;
  padding-left:25px;
  font-size:20px;
 /*  margin-top:-40px; */
 margin-top:-20px;
  color:red;
  font-weight: bold;
/*   padding-right:130px; */

}
.center-navi-item{
  width:80%;
  height:8%;
  padding-left: 20px;
  border-bottom-style:dotted;
  border-bottom-color:red;
  border-bottom-width:2px;
  display:flex;
  align-items: flex-end;
  color:red;
  font-weight: bold;
  cursor: pointer;
}
.center-biging{
  height:90%;
  width:65%;
/*   background-color:aquamarine; */
}
.center-smalling{
  height:90%;
  width:20%;
 /*  background-color: palegoldenrod; */
   display:flex;
  flex-direction: column;
  /*  justify-content: flex-end;  */
  justify-content: space-between;
}
.footer{
  width:100%;
  height:7%;
 /*  background-color:skyblue; */
 background-color: red;
  display:flex;
  flex-direction: column;
  color:white;
  align-items:center;
  justify-content:center;
  font-weight: bold;
  font-size:14px;
}
.header-up{
  width:100%;
  height:50%;
 /*  background-color: blanchedalmond; */
  display:flex;
  justify-content:space-between;
}
.header-bottom{
  width:100%;
  height:50%;
  background-color:white;
  display:flex;
  align-items:flex-end;
  border-bottom-style:solid;
  border-bottom-color:red;
}
.search{
  width:25%;
  height:100%;
  background-color:red;
  display:flex;
  justify-content: center;
  align-items:center;
}
.search-in{
  width:90%;
  height:70%;
  background-color:brown;
  border-radius:5px;
  display:flex;
  align-items:center;
  justify-content:space-around;
}
.navi-item{
  width:8%;
  height:60%;
  /* background-color: blueviolet; */
  margin-left:10px;
  display:flex;
  justify-content:center;
   align-items:center; 
   color:red;
   font-weight:bold;
   font-size:18px;
}
</style>
