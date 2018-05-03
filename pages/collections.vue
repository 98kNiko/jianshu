<template>
    <my-header></my-header>
</template>

<script>
  import myHeader from '~/components/myHeader.vue'
    export default {
       data(){
         return{
           name:'collections'
         }
       },
      components:{
         myHeader
      }
    }
</script>

<style scoped>

</style>
