<p align="center">
  <a href="https://github.com/vuejs/vue">
    <img src="https://img.shields.io/badge/vue-2.5.11-brightgreen.svg" alt="vue">
  </a>
  <a href="https://github.com/ElemeFE/element">
    <img src="https://img.shields.io/badge/element--ui-2.14.0-brightgreen.svg" alt="element-ui">
  </a>
  <a href="https://github.com/wangxiaoyi3/vue-image-verifycode//LICENSE">
    <img src="https://img.shields.io/github/license/mashape/apistatus.svg" alt="license">
  </a>
  <a href="https://github.com/wangxiaoyi3/vue-image-verifycode/releases">
    <img src="https://img.shields.io/badge/release-v1.0.1-blue" alt="GitHub release">
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

![demo](./demo.png)

## More detail

If you want to know more, you can come to this website!
[vue-image-verifycode](http://vue-image-verifycode.wangyit.com)
