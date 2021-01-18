<template>
  <div class="login-container">
    <!-- 导航栏 -->
    <van-nav-bar title="登录"
                 class="page-nav-bar" />
    <!-- 表单 -->
    <van-form @submit="onSubmit">
      <van-field name="用户名"
                 placeholder="请输入手机号">
        <i slot="left-icon"
           class="toutiao toutiao-shouji"></i>

      </van-field>
      <van-field type="password"
                 name="密码"
                 placeholder="请输入验证码">
        <i slot="left-icon"
           class="toutiao toutiao-yanzhengma"></i>
        <template #button>
          <van-button round
                      type="default"
                      class="send-sms-btn">
            获取验证码
          </van-button>
        </template>
      </van-field>
      <div style="margin: 16px;">
        <van-button block
                    type="info"
                    native-type="submit">登录</van-button>
      </div>
    </van-form>
  </div>
</template>
<script>
export default {
  name: 'LoginIndex',
  data () {
    return {

    };
  },
  methods: {
    onSubmit (values) {
      console.log('submit', values);
    },
  },
}
</script>
<style lang='less' scoped>
.login-container {
  .toutiao {
    font-size: 37px;
    color: #ccc;
  }
  .send-sms-btn {
    // background-color: #ededed;
    // background-color: red;
    width: 200px;
    height: 46px;
    line-height: 46px;
    font-size: 12px;
  }
}
</style>
