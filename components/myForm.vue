<template>
  <div>
    <form class="new-comment" method="post">
      <slot></slot>
      <textarea name="comment-content" placeholder="写下你的评论"></textarea>
      <div class="write-function-block">
        <div class="emoji-modal-wrap">
          <a href="javascript:void(0)" class="emoji" @click="emojis=!emojis">
            <i class="fa fa-smile-o" ></i>
            <div id="emojijs" v-if="emojis">
              <vue-emoji></vue-emoji>
            </div>
          </a>
          <div class="emoji-modal"></div>
        </div>
        <div class="hint">Ctrl+Enter发送</div>
        <a href="#" class="btn-send">发送</a>
        <a href="#" class="btn-cancel">取消</a>
      </div>
    </form>
  </div>
</template>
<script>
  import vueEmoji from '~/components/emoji.vue'

  export default {
    name:"myForm",
    data(){
      return {
        emojis:false,
         value: '',
        showEmoji: false,
        data: []
      }
    },
    methods: {
      selectEmoji (code) {
        this.showEmoji = false
        this.value += code
      },
      submit () {
        this.data.push(this.value)
        this.value = ''
      }
    },
    components: {
      vueEmoji
    }
  }
</script>

<style>
  .fa-smile-o{
    position: relative ;
  }
  #emojijs{
  position: absolute;
    left:-40px;
    top:100px;
  }
</style>
