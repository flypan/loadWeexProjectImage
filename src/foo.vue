<template>
  <div>
      <div class="wrapper" @click="update">
        <image :src="logoUrl" class="logo"></image>
        <text class="title">Hello {{target}}</text>
      </div>


    <!-- 导入Weex图片 -->
      <div> 
        <text> 导入Weex工程图片</text>
        <image class="airport-name-image" :src="imageLoader.loadImage('arrows_right@2x.png')"> </image>
        <image class="airport-name-image" :src="imageLoader.loadImage('ticket_order_notice@2x.png')"></image>
      </div>
  </div>

</template>

<style>
  .wrapper { align-items: center; margin-top: 120px; }
  .title { font-size: 48px; }
  .logo { width: 360px; height: 82px; }

  .airport-name-image {
    width:17wx; 
    height: 17wx;
  }

</style>

<script>

  import image from './config';

  module.exports =  {
    data () {
      return {
        imageLoader:image,

        logoUrl: 'https://alibaba.github.io/weex/img/weex_logo_blue@3x.png',
        target: 'World'
      }
    },

    methods: {
      update: function (e) {
        this.target = 'Weex'
        console.log('target:', this.target)
      }
    }
  }
</script>
