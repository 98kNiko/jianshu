<template>
    <div>
      <ul>
        <li v-for="(item,index) in meta">
          <div>
            <div class="special">
              <img src="~/assets/img/top.jpg" alt="">
              <div>
                <p>{{item.name}}</p>
                <small>简书</small>
                <span>收录了{{item.number}}K篇文章</span>
                <span>{{item.number}}K人关注</span>
              </div>
            </div>
          </div>
          <button class="fa fa-check">已关注</button>
        </li>
      </ul>
    </div>
</template>

<script>
    export default {
      data:function(){
        return{
          name:'follow',
          meta:[
            {name:'程序员',number:'2773.9'},
            {name:'@IT_互联网',number:'2773.9'},
            {name:'人文地理',number:'2773.9'},
            {name:'简书电影',number:'2773.9'},
            {name:'社会热点',number:'2773.9'},
            {name:'摄影',number:'2773.9'},
            {name:'手绘',number:'2773.9'},
            {name:'旅行_在路上',number:'2773.9'},
            {name:'自然科普',number:'2773.9'},
            {name:'原创儿童文学',number:'2773.9'},
          ]
        }
      },
    }
</script>

<style scoped>
  li>div{
    display: inline-block;
  }
.special img{
  width: 52px;
  height: 52px;
  border-radius: 5px;
}
.special{
  display: flex;
  padding: 30px 0 30px 20px;
  overflow: hidden;
}
.special>div{
  margin-left: 5px;
}

.special>div>span{
  color: #969696;
  margin-right: 5px;
  font-size: 10px;
}
  .special>div>small{
    color: #3194D0;
    padding: 0 8px;
  }
li button{
  border: 1px solid #969696;
  text-decoration: none;
  float: right;
  background: #ffffff;
  width: 100px;
  height: 39px;
  border-radius: 20px;
  color: #969696;
  margin-top: 38px;
}
</style>
