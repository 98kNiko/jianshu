<template>
    <div class="container">
      <my-header></my-header>
     <div class="containers">
       <div class="left">
         <div class="leftop">
           <div>
             <img src="~/assets/img/default-avatar.jpg"/>
           </div>
           <div class="lefts">
             <p>一个实验用名字</p>
             <div>
               <a href=""><span>0</span><span>关注 ></span></a>
               <a href=""><span>0</span><span>粉丝 ></span></a>
               <a href=""><span>0</span><span>文章 ></span></a>
               <a href=""><span>0</span><span>字数</span></a>
               <a href=""><span>0</span><span>收获喜欢</span></a>
             </div>
           </div>
         </div>
         <div class="leftbottom">
           <ul>
             <li class="fa fa-file-text"><span>文章</span></li>
             <li class="fa fa-bell-o"><span>动态</span></li>
             <li class="fa fa-comments"><span>最新评论</span></li>
             <li class="fa fa-snowflake-o"><span>热门</span></li>
           </ul>
         </div>
       </div>
       <div class="right">
         <div class="rightop">
           <a href="" class="fa fa-list-alt"><span>我关注的专题/文集/连载</span></a>
           <a href="" class="fa fa-heart-o"><span>我喜欢的文章</span></a>
         </div>
         <div class="rightbottom">
           <p>我创建的专题</p>
           <a>+<span>创建一个新专题</span></a>
         </div>
       </div>
     </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    export default {
      data:function() {
        return {
          name:'myhomepage',
        }
      },
      components:{
        myHeader,
      }
    }
</script>

<style scoped>
  .containers{
    display: flex;
  }
  .left{
    margin-top: 80px;
    width: 60%;
  }
  .left .leftop{
    display: flex;
    margin-bottom:20px;
  }
  .left .leftop img{
    border-radius: 50%;
    margin-right: 20px;
  }
  .left .leftop>.lefts p{
    font-size: 25px;
  }
  .left .leftop>.lefts>div span{
    display: block;
    font-size: 10px;
  }
  .left .leftop>.lefts span:nth-of-type(2){
    color: #969696;
  }

  .left .leftop>.lefts>div>a{
    display: inline-block;
    border-right: 1px solid #F0F0F0;
    padding:0 10px 0 5px;

  }
  .left .leftop>.lefts>div>a:nth-last-of-type(1){
    border: none;
  }
  .left .leftbottom{
    display: block;
    padding-bottom: 20px;
    border-bottom: 1px solid #f0f0f0;
  }
  .left .leftbottom ul li{
    display: inline-block;
    color: #969696;
    font-size: 17px;
    margin:0 15px;
  }
  .left .leftbottom ul li span{
    padding-left: 5px;
  }
  .right{
    display: inline-block;
    margin-top:80px;
    overflow: hidden;
  }
  .right>.rightop{
    border-top: 1px solid #f0f0f0;
    border-bottom: 1px solid #f0f0f0;
  }
  .right>.rightop a{
    display: block;
    margin: 25px 15px;
  }
  .right>.rightop>a span{
    margin-left: 10px;
  }
  .right .rightbottom {
    padding: 20px;
    border-bottom: 1px solid #f0f0f0;
  }
  .right .rightbottom>p{
    font-size: 15px;
    color: #969696;
    margin-bottom: 10px;
  }
  .right .rightbottom>a{
    color: #42C068;
    font-size: 16px;
  }
  .right .rightbottom>a>span{
    margin-left: 5px;
  }

</style>
