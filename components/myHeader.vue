<template>
  <div>
    <nav class="navbar navbar-fixed-top">
      <div class="width-limit">
        <!-- logo -->
        <nuxt-link  class="logo" to="/">
          <img src="~/assets/img/navlogo.png" >
        </nuxt-link>
        <!--右上角，写文章-->
        <nuxt-link to="/write" class="write-btn">
          <i class="fa fa-edit"></i>
          写文章
        </nuxt-link>
        <!--登录用户信息-->
        <div class="user" @mouseleave="isShow=false" @mouseover="isShow=true">
          <div class="drop-down">
            <nuxt-link to="/u/123" class="avatar">
              <img src="~/assets/img/top.jpg" >
            </nuxt-link>
          </div>
          <ul class="drop-menu" v-show="isShow">
            <li>
              <nuxt-link to="/">
                <i class="fa fa-home"></i>
                我的主页
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/">
                <i class="fa fa-bookmark"></i>
                收藏的文章
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/bookmarks">
                <i class="fa fa-heart"></i>
                喜欢的文章
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/settings/basic">
                <i class="fa fa-cog"></i>
                设置
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/sign-out">
                <i class="fa fa-sign-out"></i>
                退出
              </nuxt-link>
            </li>
          </ul>
        </div>
        <!--右上角，登录注册-->
        <!--导航部分-->
        <div class="container">
          <div class="nav-listtop">
            <button type="button" @click="tt">
              <span class="fa fa-bars"></span>
            </button>
          </div>
          <ul  :class="{'nav-list':true,'navlisttwo':navlisttwo==1}">
            <li>
              <nuxt-link class="active" to="/">
                <i class="fa fa-compass"></i>
                <span>发现</span>
              </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/follow">
                <i class="fa fa-book"></i>
                <span>关注</span>
              </nuxt-link>
            </li>
            <li class="user" @mouseover="userShow=true" @mouseleave="userShow=false">
              <nuxt-link to="/noify">
                <i class="fa fa-bell-o"></i>
                <span>消息</span>
              </nuxt-link>
              <ul class="drop-menu" v-show="userShow">
                <li>
                  <nuxt-link to="/">
                    <i class="fa fa-comment-o"></i>
                    评论
                  </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="/">
                    <i class="fa fa-envelope-o"></i>
                    简讯
                  </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="/">
                    <i class="fa fa-square-o"></i>
                    关注
                  </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="/">
                    <i class="fa fa-heart-o"></i>
                    喜欢和赞
                  </nuxt-link>
                </li>
              </ul>
            </li>
            <li class="search">
              <form method="post">
                <input type="text" placeholder="搜索" class="search-input">
                <a href="#" class="search-btn">
            <li class="fa fa-search"></li>
            </a>
            </form>
            </li>
          </ul></div>
      </div>
    </nav>
  </div>
</template>
<script>
  export default{
    name:'myHeader',
    data:function () {
      return{
        isShow:false,
        userShow:false,
        navlisttwo:true
      }
    },
    methods:{
      tt:function () {
        this.navlisttwo=~this.navlisttwo;
      }
    }
  }
</script>
<style scoped>
  nav{
    width: 100%;
    height: 56px;
  }
  .navbar{
    margin-bottom: 20px;
    border-bottom:1px solid #f0f0f0;
    background-color: #fff
  }
  .navbar::before{
    content: '';
    display: table;
  }
  .navbar-fixed-top{
    position: fixed;
    left: 0;
    top: 0;
    z-index:9999;
  }
  nav .width-limit{
    min-width: 768px;
    max-width: 1440px;

    margin: 0 auto;
  }
  nav .logo{
    float: left;
    height: 56px;
    display: block;
  }
  nav .logo img{
    height: 100%;
  }
  nav .write-btn{
    float: right;
    width: 100px;
    height: 40px;
    line-height: 40px;
    margin: 8px 15px 0;
    border-radius: 20px;
    font-size: 15px;
    color: #fff;
    background: #ea6f5a;
    text-align: center;
  }
  nav .write-btn:hover{
    background: rgb(236,74,93);
  }
  nav .user{
    position: relative;
    float: right;
  }
  nav .user .avatar{
    position: relative;
    display: block;
    width: 40px;
    height: 40px;
    margin: 8px 28px 8px 20px;
  }
  nav .user .avatar:before{
    content:'';
    position: absolute;
    border-left: 5px solid transparent;
    border-right: 5px solid transparent;
    border-top: 5px solid #999;
    top:18px;
    right: -14px;
  }
  nav .user .avatar img{
    width: 100%;
    height: 100%;
    border-radius: 50%;
    border: 1px solid #eee;
  }
  nav .user:hover{
    background-color: #f5f5f5;
  }
  nav .user .drop-menu{
    position: absolute;
    left: 0;
    box-shadow: 0 0 8px rgba(0,0,0,.1);
    min-width: 160px;
    z-index: 999;
    margin: 0;
    padding: 10px 0;
    font-size: 15px;
  }
  nav .user .drop-menu li a{
    padding: 10px 20px;
    line-height: 30px;
    display: block;
  }
  nav .user .drop-menu li a:hove{
    background: #f5f5f5;
  }
  nav .user .drop-menu li a i{
    margin-right: 10px;
    color: #ea6f5a;
    width: 20px;
    height: 20;
    font-size: 20px;
    display: inline-block;
  }
  nav .nav-list{
    margin: 0;
    transition: height 0.5s;
  }
  nav .nav-list:after{
    content: "";
    height: 0;
    display: block;
    visibility: hidden;
    clear: both;
  }
  nav .nav-list>li{
    float: left;
    margin-right: 5px;
  }
  nav .nav-list>li a{
    display: block;
    height: 56px;
    line-height: 26px;
    padding: 15px;
  }
  nav .nav-list>li a.active{
    color: #ea6f5a;
    background:none!important;
  }
  nav .nav-list>li a:hover{
    background: #f5f5f5;
  }
  nav .nav-list>li a i{
    margin-right: 5px;
    font-size: 20px;
  }
  nav .nav-list .search{
    padding-left: 15px;
    margin-right: 10px;
  }

  nav  .nav-list .search form{
    margin-bottom: 20px;
    position: relative;
    top: 10px;
  }
  nav .nav-list .search form .search-input{
    width: 240px;
    height: 38px;
    font-size: 14px;
    padding: 0 40px 0 20px;
    border: 1px solid #eee;
    background:#eee;
    border-radius: 40px;
    transition: width .5s;
  }
  nav .nav-list .search form .search-input:focus{
    width: 320px;
  }
  nav .nav-list .search form .search-input:focus~.search-btn{
    background-color: #969696;
    color: #fff;
    border-radius: 50%;
}

  nav .nav-list .search form .search-btn{
    position: absolute;
    width: 30px;
    height: 30px;
    top: 4px;
    right: 5px;
    color: #969696;
    text-align: center;
    padding: 0;
  }
  nav .nav-list .search form .search-btn:hover{
    background: none;
  }

  nav .nav-list .search form .search-btn i{
  display: block!important;
  margin: 0;
  text-align: center;
  line-height: 30px;
  font-size: 15px;
}
  .nav-listtop{
    display: none;
  }

  .nav-listtop>button{
    border: 0.5px solid #DDDDDD;
    background-color: #ffffff;
    margin-top: 8px;
    border-radius: 4px;
  }
  .nav-listtop>button:hover{
    background-color: #DDDDDD;

  }
  .nav-listtop>button span:hover{
    background-color: #DDDDDD;

  }
  .nav-listtop>button span{
    margin-top: 9px 15px 8px 0;
    padding: 10px 10px;
    background-color: #ffffff;
    border: 1px solid #DDDDDD;
    border: none;
    color: #888888;
    font-size: 18px;
  }


  @media (max-width: 1440px) {
    nav .nav-list>li a i{
     display: none;
    }
    nav .nav-list .search form .search-input{
      width: 160px;
    }
    nav .nav-list .search form .search-input:focus{
      width: 240px;
    }

  }
  @media (max-width:1080px) {
    nav .nav-list li span{
      display:none;
    }
    nav .nav-list>li a i{
      display: block;
    }
  }

  @media (max-width:768px) {
   .navlisttwo{
     display: none;
   }
    .nav-listtop{
      display: block;
    }
    nav .nav-list li span{
      display:block;
    }
    nav .nav-list>li a i{
      display: none;
    }
    .nav-list>li{
      width: 100%;
      text-align: center;
      background-color: #FFFFFF;
      border-bottom: 1px solid #f0f0f0;
    }
    .container{
      padding: 0;
      margin: 0;
    }
    .nav-list>.user>.drop-menu{
      display: none;
    }
    nav .nav-list .search form .search-input{
      width: 719px;
    }
    nav .nav-list .search form .search-input:focus{
      width: 719px;
    }
  }


</style>


