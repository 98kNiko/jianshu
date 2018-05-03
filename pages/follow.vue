<template>
   <div class="container">
     <my-header></my-header>
     <div class="follow">
       <div class="right">
         <p>全部关注<span class="fa fa-chevron-circle-down"></span></p>
         <ul>
           <li><img src="~/assets/img/top.jpg" alt=""><span>添加关注</span></li>
           <li v-for="(item,index) in meta">
             <img src="~/assets/img/top.jpg" alt="">
             <span>{{item.name}}</span>
           </li>
         </ul>
       </div>
       <div class="left">
         <ul>
           <li>全部推荐</li>
           <li>推荐作者</li>
           <li>推荐专题</li>
         </ul>
         <ul>
           <li v-for="(item,index) in meta">
             <div class="special">
               <img src="~/assets/img/top.jpg" alt="">
            <div>
              <p>{{item.name}}</p>
              <h6>{{item.content}}</h6>
              <span>{{item.number}}K篇文章</span>
              <span>{{item.number}}K人关注</span>
            </div>
             </div>
             <button>+ 关注</button>
           </li>
         </ul>
       </div>
    </div>
   </div>
</template>

<script>
  import myHeader from '~/components/myHeader'
    export default {
        data:function(){
          return{
            name:'follow',
            meta:[
              {name:'程序员',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'@IT_互联网',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'人文地理',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'简书电影',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'社会热点',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'摄影',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'手绘',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'旅行_在路上',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
              {name:'自然科普',content:'本专题仅收涉及自然科学（生物、天文、物理等）的科普、介绍、发现类...',number:'2773.9'},
              {name:'原创儿童文学',content:'欢迎关注公众号简宝玉( 公众号ID : jianshu4321 ...',number:'2773.9'},
            ]
          }
        },

      components:{
          myHeader
      }
    }
</script>

<style scoped>
  .container .nav-list>li:nth-of-type(1)>a>i{
    color: black!important;
  }
  .container .nav-list>li:nth-of-type(2)>a>i{
    color: #EA6F5A!important;
  }
  .container .follow{
    margin-top: 80px;
    display: flex;
  }
  .right{
    width: 30%;
    border-right: 1px solid #f0f0f0;
  }
  .right p{
    margin-bottom: 10px;
  }
  .right p>span{
    margin-left: 5px;
  }
  .right ul>li:nth-of-type(1) img{
    border-radius: 50%;
  }
  .right ul>li img {
    border-radius: 5px;
    width: 40px;
    height: 40px;
  }
  .right ul>li{
    padding: 10px;
    display: flex;
    align-items: center;
  }
  .right ul>li span{
    margin-left: 10px;
  }
  .right ul>li:hover{
    background:#f0f0f0;
  }
  .right ul>li:nth-of-type(1){
    background: #f0f0f0;
  }
  .left ul{
    border-bottom: 1px solid #f0f0f0;
  }
  .left ul:nth-of-type(1)>li{
    display: inline-block;
    margin: 30px  0px 15px 45px ;
    color: #969696;
  }
  .left ul:nth-of-type(2){
    margin-left: 45px;
  }
  .left ul:nth-of-type(2)>li{
    display: flex;
    justify-content: space-between;
  }
  .left ul:nth-of-type(2)>li img{
    width: 52px;
    height: 52px;
    border-radius: 5px;
  }
  .left ul:nth-of-type(2)>li .special{
    display: flex;
    padding: 30px 0;
  }
  .left ul:nth-of-type(2)>li .special>div{
    margin-left: 5px;
  }
  .left ul:nth-of-type(2)>li .special>div>h6{
      color: #969696;
    font-size: 10px;
  }
  .left ul:nth-of-type(2)>li .special>div>span{
    color: #969696;
    margin-right: 5px;
    font-size: 10px;
  }
  .left ul:nth-of-type(2)>li button{
    border: none;
    background: #42c02e;
    width: 100px;
    height: 39px;
    border-radius: 20px;
    color: white;
    margin-top: 35px;
  }
</style>
