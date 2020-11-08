<template>
  <div class="image-verify-code-container" @click="refreshImageVerifyCode" @mouseenter="showMask" @mouseleave="showMask">
    <img v-bind:style="imageStyle" class="image-container" :src="imageVerifyCodeUrl" title="刷新验证码"/>
    <transition name="el-fade-in-linear">
      <div v-if="maskEnable">
        <div v-bind:style="maskStyle" class="mask" v-if="maskIsShow">
          <i v-bind:style="iconHeight" v-bind:class="refreshIcon" class="refresh-btn"></i>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
  export default {
    name: "vue-image-verifycode",
    props: {
      url: {
        type: String,
        required: true
      },
      radius: {
        type: String | Number,
        default: '4px' | 4
      },
      mask: {
        type: Boolean,
        default: true
      },
      maskColor: {
        type: String,
        default: 'rgba(87, 87, 87, 0.5)'
      },
      refresh: {
        type: Boolean,
        default: true
      },
      iconSrc: {
        type: String,
        default: 'el-icon-refresh-right'
      },
      iconColor: {
        type: String,
        default: 'rgba(255, 255, 255, 0.8)'
      },
      iconSize: {
        type: String | Number,
        default: '24px' | 24
      }
    },
    data() {
      return {
        imageVerifyCodeUrl: '',
        maskIsShow: false,
        icon: this.icon,
      }
    },
    mounted() {
      this.refreshImageVerifyCode();
    },
    methods: {
      refreshImageVerifyCode() {
        if (this.refreshEnable) {
          this.imageVerifyCodeUrl = this.url + '?time=' + Date.now();
        }
      },
      showMask() {
        if (this.maskIsShow)
          this.maskIsShow = false;
        else
          this.maskIsShow = true
      },
      formatValue(val) {
        return val.type === String? val : val + 'px'
      }
    },
    computed: {
      maskStyle() {
        return {
          'border-radius': this.formatValue(this.radius),
          'font-size': this.formatValue(this.iconSize),
          'background-color': this.maskColor,
          'color': this.iconColor
        }
      },
      imageStyle() {
        return {
          'border-radius': this.formatValue(this.radius)
        }
      },
      iconHeight() {
        return {
          'height': this.formatValue(this.iconSize)
        }
      },
      maskEnable() {
        return this.mask
      },
      refreshIcon() {
        return this.iconSrc
      },
      refreshEnable() {
        return this.refresh
      }
    }
  };
</script>

<style scoped>
  .image-verify-code-container {
    width: 100%;
    height: 100%;
    position: relative;
    cursor: pointer;
  }
  .image-container {
    width: 100%;
    height: 100%;
  }
  .mask {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    text-align: center;
    user-select: none;
  }
  .refresh-btn {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    margin: auto;
  }
</style>
