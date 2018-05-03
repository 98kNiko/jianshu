<template>
  <div class="container">
    <my-header></my-header>
    <div class="collects">
      <img src="~/assets/img/collect.png"/>
    </div>
  </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    export default {
      data:function () {
        return {
          name:'collect',
        }
      },
      components:{
        myHeader
      }
    }
</script>

<style scoped>
  .collects{
    text-align: center;
  }
  .collects img{
  margin-top: 80px;
  width:690px;
  height: 110px;
  }
  @media (max-width:1080px) {
    .collects img {
      width: 532px;
      height: 85px;
    }
  }
</style>
