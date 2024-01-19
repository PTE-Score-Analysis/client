<template>
  <view class="loginPage">
    <view class="loginPageBody">
      <view class="upperPage">
        <view class="loginGreeting">
          <view class="loginText">
            登录
          </view>
          <text class="loginCatchline">开启趣味学习体验</text>
        </view>
      </view>

      <view class=" midPage">
        <view class="wechatLogin">
          <button class="loginBtn" hover-class="clickEffect">
            <text class="wechatLoginText"><span class="mui-icon mui-icon-weixin"></span> 微信登陆</text>
          </button>
        </view>

        <view class="consent">
          <view class="checkbox">
            <checkbox-group bindchange="checkboxChange">
              <checkbox value="agree" />
              <text class="greyText">同意</text>
              <text class="blueText" bindtap='toprotocol'>用户协议</text>
              <text class="greyText">、</text>
              <text class="blueText" bindtap='toprotocol'>隐私政策</text>
              <text class="greyText">和</text>
              <text class="blueText" bindtap='toprotocol'>儿童保护政策</text>
            </checkbox-group>
          </view>
        </view>
      </view>

      <view class="lowerPage">
        <view class="thirdParty">
          <view class="greyText other">
            <text class="greyText">———————其他登陆方式———————</text>
            <view class="thirdPartyLogin">
              <button class="thirdPartyLoginBtn">
                <icon class="thirdPartyLoginBtn mui-icon mui-icon-locked"></icon>
              </button>
              <text class="greyText">账号密码</text>
            </view>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script lang="ts">
  export default {
    data() {
      return {

      };
    }
  }
</script>

<style>
  @import "login.scss"
</style>