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
@font-face {
  font-family: 'iconfont';
  src: url('https://at.alicdn.com/t/font_865816_17gjspmmrkti.ttf') format('truetype');
}
* {
  box-sizing: border-box;
  margin: 0px;
  padding: 0px;
}
.login-title {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.login-title text:first-child {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 10px;
}
.login-title text:nth-child(2) {
  font-size: 12px;
  color: #9fa3a9;
}
.login-form {
  margin-top: 50px;
}
input {
  background-color: #f6f6f6;
  max-width: 335px;
  height: 60px;
  margin: 10px 20px;
  font-size: 16px;
}

.icon-eye {
  font-size: 50px;
}

.password-input {
  position: relative;
}
.icon-eye {
  position: absolute;
  top: 50%;
  right: 30px;
  z-index: 1;
  transform: translateY(-50%);
}
.btn {
  background-color: #265ae8;
  max-width: 335px;
  height: 60px;
  color: #ffffff;
  margin: 10px 20px;
}
a {
  text-align: center;
  text-decoration: none;
  font-size: 12px;
  color: #265ae8;
}
.other-login-container {
  position: relative;
  min-height: 30px;
  text-align: center;
  margin-top: 150px;
}
.line {
  content: '';
  position: absolute;
  top: 50%;
  left: 0;
  transform: translateY(-50%);
  max-width: 335px;
  height: 1px;
  background-color: #9fa3a9;
}
.other-login {
  text-align: center;
  color: #9fa3a9;
  font-size: 12px;
  z-index: 1;
}
.wechat-icon {
  width: 45px;
  height: 45px;
  background-color: #f7f7f7;
  border-radius: 50%;
  text-align: center;

  margin: 10px auto;
}
.wechat-text {
  color: #9fa3a9;
  font-size: 12px;
  text-align: center;
}
</style>
