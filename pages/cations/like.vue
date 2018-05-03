<template>
  <div class="container">
    <my-header></my-header>
    <div>
      <ul class="left">
        <nuxt-link to="/cations/comment">
          <li class="fa fa-comment-o">
            <span>评论</span>
          </li>
        </nuxt-link>
        <nuxt-link to="/cations/news">
          <li class="fa fa-envelope-o">
            <span>简讯</span>
          </li>
        </nuxt-link>
        <nuxt-link to="/cations/attention">
          <li class="fa fa-square-o">
            <span>关注</span>
          </li>
        </nuxt-link>
        <nuxt-link to="/cations/like">
          <li class="fa fa-heart-o">
            <span>喜欢和赞</span>
          </li>
        </nuxt-link>
      </ul>
      <div class="right">
        <p>收到的喜欢和赞</p>
      </div>
    </div>
  </div>
</template>

<script>
  import myHeader from '~/components/myHeader'
  export default {
    data () {
      return {
        name:'cations',
      }
    },
    components:{
      myHeader,
    }
  }
</script>

<style scoped>
  .container>div{
    display: flex;
  }
  .left{
    margin-top: 80px;
    width: 30%;
  }
  .left li{
    display: block;
    font-size: 16px;
    color: #EA6F5A;
    padding: 20px;
  }
  .left a:nth-of-type(4)>li{
    background:#f0f0f0 ;
  }
  .left li:hover{
    background: #f0f0f0;
  }
  .left li span{
    margin-left:10px;
    color: black;
  }
  .right{
    margin-top: 80px;
    margin-left: 20px;
  }
</style>

