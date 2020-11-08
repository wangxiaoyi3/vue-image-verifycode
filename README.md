<p align="center">
  <a href="https://github.com/vuejs/vue">
    <img src="https://img.shields.io/badge/vue-2.5.11-brightgreen.svg" alt="vue">
  </a>
  <a href="https://github.com/ElemeFE/element">
    <img src="https://img.shields.io/badge/element--ui-2.14.0-brightgreen.svg" alt="element-ui">
  </a>
  <a href="https://github.com/wangxiaoyi3/vue-image-verifycode/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/mashape/apistatus.svg" alt="license">
  </a>
  <a href="https://github.com/wangxiaoyi3/vue-image-verifycode/releases">
    <img src="https://img.shields.io/badge/release-v1.0.2-blue" alt="GitHub release">
  </a>
</p>

# vue-image-verifycode

> An Image VerifyCode Component based on Vue.js and Element UI

## Install

``` bash
# install dependencies
npm install vue-image-verifycode --save
```

## Example

main.js

``` javascript
import ImageVerifyCode from 'vue-image-verifycode'
Vue.use(ImageVerifyCode)
```
App.vue

``` vue
<vue-image-verifycode :url="url"></vue-image-verifycode>
```

``` javascript
data() {
  return {
     url: 'https://xxxx' //Change to your image URL
   }
 }
```
demo

![demo](https://github.com/wangxiaoyi3/vue-image-verifycode/blob/master/demo.png)

## Attribute

|参数        |说明        |类型       |可选值       |默认值       |
|:----------:|:-------------:|:-----------:|:-----------:|:-----------:|
|url        |图形验证码接口地址，必填属性|string|—|—|
|radius     |验证码容器的圆角大小，建议4px，和element ui的组件圆角大小保持一致|string/number|—|4px/4|
|mask       |鼠标悬浮时是否显示遮罩层|boolean|—|true|
|mask-color |遮罩层背景颜色，支持RGB,RGBA,16进制颜色|string|—|rgba(87, 87, 87, 0.5)|
|refresh    |点击是否刷新验证码|boolean|—|true|
|icon-src   |遮罩层中的刷新图标，使用element ui icon的class名称|string|—|	el-icon-refresh-right|
|icon-color |遮罩层中的刷新图标颜色，与mask-color使用方法一致|string|—|rgba(255, 255, 255, 0.8)|
|icon-size  |遮罩层中的刷新图标大小，建议24px|string/number|—|24px/24|

## More detail

If you want to know more, you can come to this website!
[vue-image-verifycode](http://vue-image-verifycode.wangyit.com)
