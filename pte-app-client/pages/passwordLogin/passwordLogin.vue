<template>
  <view>
    <view class="login-title">
      <text>账号密码登录</text>
      <text>开启趣味学习体验</text>
    </view>
    <view class="login-form">
      <form @submit="formSubmit">
        <view class="">
          <input class="account-input" name="input" placeholder="请输入用户名" />
        </view>
        <view class="uni-form-item uni-column">
          <view class="password-input">
            <input class="" placeholder="请输入密码" :password="showPassword" />
            <!-- <text class="uni-icon" :class="[!showPassword ? 'uni-eye-active' : '']" @click="changePassword">&#xe568;</text> -->
            <uni-icons class="icon-eye" type="eye-slash" size="24"></uni-icons>
          </view>
        </view>
        <view>
          <button class="btn" form-type="submit">登录</button>
        </view>
      </form>
      <view>
        <navigator url="#" hover-class="navigator-hover">
          <a type="default">忘记密码</a>
        </navigator>
      </view>
    </view>
    <view class="other-login-container">
      <view class="line"></view>
      <text class="other-login">------------------其他登录方式------------------</text>
    </view>
    <view>
      <view class="wechat-icon">
        <uni-icons custom-prefix="iconfont" type="icon-weixin" size="30" color="#069607"></uni-icons>
      </view>
      <view class="wechat-text">
        <text class="">微信</text>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      showPassword: true
    };
  },
  methods: {
    changePassword: function () {
      this.showPassword = !this.showPassword;
    }
  }
};
</script>

<style>
@import'./passwordLogin.scss';
</style>
