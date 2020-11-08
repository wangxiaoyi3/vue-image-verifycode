<template>
  <div id="app">
    <div class="demo-container">
      <h2>vue-image-verifycode</h2>
      <el-input class="code-input" placeholder="图形验证码"></el-input>
      <div class="code-image">
        <ImageVerifyCode :url="url"></ImageVerifyCode>
      </div>
    </div>
  </div>
</template>

<script>
import ImageVerifyCode from "./lib/ImageVerifyCode";
export default {

  name: 'app',
  components: {ImageVerifyCode},
  data () {
    return {
      url: 'http://192.168.0.107:8081/verifyCode/image' //换成自己对应的验证码地址
    }
  }
}
</script>

<style>
  .demo-container {
    width: 300px;
    margin: 0 auto;
  }
  .code-input {
    width: 60%;
  }
  .code-image {
    float: right;
    height: 40px; /* 建议给验证码外层容器设置高度 */
  }
</style>
