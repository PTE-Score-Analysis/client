<template>
  <view class="changePwdPage">
    <view class="changePwdPageBody">
      <view class="title">更改密码</view>
      <view class="inputSection">
        <view class="inputRow"> 
          <input class="inputField" :type="passwordVisible ? 'text' : 'password'" placeholder="输入初始密码" />
          <image class="eyeIcon" src="/static/eye.png" @click="togglePasswordVisibility"></image> <!-- 修改这里 -->
        </view>
        <text class="errorMsg">与初始密码不匹配</text>
      </view>

      <view class="inputSection">
        <view class="inputRow"> 
          <input class="inputField" :type="passwordVisible ? 'text' : 'password'" placeholder="输入新密码" />
          <image class="eyeIcon" src="/static/eye.png" @click="togglePasswordVisibility"></image> <!-- 修改这里 -->
        </view>
        <text class="errorMsg">必须包含8个字符</text>
      </view>

      <view class="inputSection">
        <view class="inputRow"> 
          <input class="inputField" :type="passwordVisible ? 'text' : 'password'" placeholder="再次输入新密码" />
          <image class="eyeIcon" src="/static/eye.png" @click="togglePasswordVisibility"></image> <!-- 修改这里 -->
        </view>
        <text class="errorMsg">与上一次输入的密码不匹配</text>
      </view>

      <button class="submitBtn">确定更改</button>
    </view>
  </view>
</template>

<script lang="ts">
export default {
  data() {
    return {
      passwordVisible: false as boolean, 
    };
  },
  methods: {
    togglePasswordVisibility() {
      this.passwordVisible = !this.passwordVisible;
    },
  },
};
</script>

<style>
@import "changePwd.css";
</style>
