<template>
  <view class="loginPage">
    <view class="loginPageBody">
      <view class="upperPage">
        <!--        <view class="returnButtun">
        commented because the return butten can be generated automatically
        </view> -->
        <view class="loginGreeting">
          <view class="loginText"> 登录 </view>
          <text class="loginCatchline">开启趣味学习体验</text>
        </view>
      </view>

      <view class="midPage">
        <view class="wechatLogin">
          <text class="wechatText">微信</text>
          <button class="loginBtn" hover-class="clickEffect">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="20"
              viewBox="0 0 24 20"
              fill="none"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M16.8528 5.90876C16.586 5.87893 16.3169 5.85904 16.045 5.85904C12.0603 5.85904 8.913 8.83322 8.91302 12.4982C8.91302 13.1075 9.00793 13.695 9.17191 14.2559C8.91304 14.2761 8.65203 14.2891 8.38876 14.2891C7.50793 14.2891 6.77224 14.1381 5.93625 13.9665L5.93624 13.9665C5.77838 13.9341 5.61694 13.9009 5.45027 13.8679L2.51774 15.3384L3.3568 12.815C1.25673 11.3476 -3.05176e-05 9.4558 -3.05176e-05 7.15201C-3.05176e-05 3.16075 3.77739 0.0177307 8.38874 0.0177307C12.5134 0.0177307 16.1271 2.52892 16.8528 5.90876ZM12.5846 4.63149C12.5846 4.00027 12.1662 3.58468 11.5346 3.58468C10.9057 3.58468 10.2749 4.00008 10.2749 4.63149C10.2749 5.26021 10.9057 5.68146 11.5346 5.68146C12.1662 5.68146 12.5846 5.26021 12.5846 4.63149ZM5.66351 5.68143C5.03479 5.68143 4.40026 5.26018 4.40026 4.63135C4.40026 4.00008 5.03482 3.58466 5.66351 3.58466C6.29224 3.58466 6.71068 4.00008 6.71068 4.63135C6.71072 5.26018 6.29224 5.68143 5.66351 5.68143ZM16.5759 6.30977C20.3453 6.30977 23.7013 9.0434 23.7013 12.3972C23.7013 14.289 22.4468 15.9641 20.763 17.2275L21.3938 19.3238L19.0929 18.0638C18.254 18.2742 17.4113 18.4848 16.5759 18.4848C12.5845 18.4848 9.44097 15.7568 9.44097 12.3972C9.44097 9.0434 12.5845 6.30977 16.5759 6.30977ZM14.2626 11.3476C13.8448 11.3476 13.4235 10.9321 13.4235 10.5082C13.4235 10.0903 13.8449 9.66935 14.2626 9.66935C14.8971 9.66935 15.3126 10.0903 15.3126 10.5082C15.3127 10.9321 14.8971 11.3476 14.2626 11.3476ZM18.0436 10.5082C18.0436 10.9321 18.462 11.3476 18.8768 11.3476C19.5055 11.3476 19.9268 10.9321 19.9268 10.5082C19.9268 10.0903 19.5056 9.66935 18.8768 9.66935C18.4621 9.66935 18.0436 10.0903 18.0436 10.5082Z"
                fill="white"
              />
            </svg>
            <text class="wechatLoginText"> 微信登陆</text>
          </button>
        </view>

        <view class="consent">
          <view class="consentTitle"> 用户协议 </view>
          <view class="checkbox">
            <checkbox-group bindchange="checkboxChange">
              <checkbox value="agree" />
              <text class="greyText">同意</text>
              <text class="blueText" bindtap="toprotocol">用户协议</text>
              <text class="greyText">、</text>
              <text class="blueText" bindtap="toprotocol">隐私政策</text>
              <text class="greyText">和</text>
              <text class="blueText" bindtap="toprotocol">儿童保护政策</text>
            </checkbox-group>
          </view>
        </view>
      </view>

      <view class="lowerPage">
        <view class="thirdParty">
          <text class="greyText">第三方</text>
          <view class="greyText other">
            <text class="greyText">———————其他登陆方式———————</text>
            <view class="thirdPartyLogin">
              <button class="thirdPartyLoginBtn">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="45"
                  height="45"
                  viewBox="3 3 45 45"
                  fill="none"
                >
                  <circle cx="22.5" cy="22.5" r="22.5" fill="#F7F7F7" />
                  <path
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M17.4281 18.846V16.2341C17.4281 13.349 19.7669 11.0102 22.652 11.0102C25.5371 11.0102 27.8759 13.349 27.8759 16.2341V18.846H30.4878C31.2091 18.846 31.7938 19.4307 31.7938 20.152V30.5997C31.7938 31.321 31.2091 31.9057 30.4878 31.9057H14.8162C14.0949 31.9057 13.5102 31.321 13.5102 30.5997V20.152C13.5102 19.8056 13.6478 19.4734 13.8927 19.2285C14.1376 18.9836 14.4698 18.846 14.8162 18.846H17.4281ZM21.999 26.5708V28.6408C21.999 29.0014 22.2914 29.2938 22.652 29.2938C23.0126 29.2938 23.305 29.0014 23.305 28.6408V26.5708C24.2049 26.2528 24.7447 25.3327 24.5834 24.392C24.422 23.4512 23.6064 22.7636 22.652 22.7636C21.6975 22.7636 20.8819 23.4512 20.7206 24.392C20.5592 25.3327 21.0991 26.2528 21.999 26.5708ZM25.9169 16.2341V18.846H19.3871V16.2341C19.3871 14.4309 20.8488 12.9691 22.652 12.9691C24.4552 12.9691 25.9169 14.4309 25.9169 16.2341Z"
                    fill="#2A2A37"
                  />
                </svg>
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
    return {};
  },
};
</script>

<style>
@import "login.css";
</style>