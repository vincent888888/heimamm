<template>
  <div class="login">
    <div class="left">
      <div class="top">
        <img class="logo" src="@/assets/img/login_logo.png" alt />
        <span class="t1">黑马面面</span>
        <div class="line"></div>
        <span class="t2">用户登陆</span>
      </div>
      <div class="bd">
        <el-form ref="form" :model="form" label-width="0px">
          <el-form-item >
            <el-input placeholder="请输入手机号" prefix-icon="el-icon-user" v-model="form.usname"></el-input>
          </el-form-item>
          <el-form-item>
            <el-input
              placeholder="请输入密码"
              prefix-icon="el-icon-lock"
              show-password
              v-model="form.pswd"
            ></el-input>
          </el-form-item>
          <el-form-item>
            <el-row>
              <el-col :span="16">
                <el-input
                  placeholder="请输入验证码"
                  prefix-icon="el-icon-key"
                  show-password
                  v-model="form.code"
                ></el-input>
              </el-col>
              <el-col :span="8">
                <img class="img" src="http://123.57.150.216:8567/captcha?type=login" alt />
              </el-col>
            </el-row>
          </el-form-item>
          <el-form-item label-width="0px">
            <el-checkbox v-model="checked">
              我已阅读并同意
              <el-link type="primary">用户协议</el-link>和
              <el-link type="primary">隐私条款</el-link>
            </el-checkbox>
          </el-form-item>
          <el-form-item label-width="0px">
            <el-button class="btn" type="primary">登录</el-button>
            <br />
            <el-button class="btn" type="primary">注册</el-button>
          </el-form-item>
        </el-form>
      </div>
    </div>
    <img class="right" src="@/assets/img/login_banner_ele.png" alt />
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        usname: "",
        pswd: "",
        code: ""
      }
    };
  }
};
</script>

<style lang="less">
.login {
  width: 100%;
  height: 100%;
  background: linear-gradient(
    225deg,
    rgba(20, 148, 250, 1),
    rgba(2, 198, 250, 1)
  );
  display: flex;
  justify-content: space-around;
  align-items: center;
  .left {
    width: 478px;
    height: 550px;
    background: rgba(245, 245, 245, 1);
    padding: 43px;
    .top {
      display: flex;
      align-items: center;
      .logo {
        width: 22px;
        height: 17px;
      }
      .t1 {
        font-size: 24px;
        font-family: SourceHanSansCN;
        font-weight: 400;
        color: rgba(13, 12, 12, 1);
        margin: 0 14px 0 17px;
      }
      .line {
        width: 1px;
        height: 28px;
        margin-right: 14px;
        background: rgba(199, 199, 199, 1);
      }
      .t2 {
        font-size: 22px;
        font-family: PingFangSC;
        font-weight: 400;
        color: rgba(13, 12, 12, 1);
      }
    }
    .bd {
      margin-top: 20px;
      .img {
        height: 100%;
        width: 100%;
      }
      .btn {
        width: 100%;
        margin-bottom: 20px;
      }
    }
  }
  .right {
    width: 633px;
    height: 435px;
  }
}
</style>