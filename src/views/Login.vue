<template>
  <div class="login">
    <header class="header">
      <div class="logo">
        <div class="tb-logo">
          <img src="../static/image/login-logo.png" alt="...">
        </div>
      </div>
    </header>
    <div class="form" v-if="isAccount">
      <label>
        <input class="clear" type="text" placeholder="手机号/邮箱/会员名" v-model="username">
      </label>
      <label>
        <input class="clear" type="password" placeholder="请输入登录密码" v-model="password">
      </label>
    </div>
    <div class="form" v-if="!isAccount">
      <label>
        <input class="clear" type="text" placeholder="请输入手机号" v-model="phone">
      </label>
      <label>
        <input class="clear" type="password" placeholder="请输入验证码" v-model="captcha">
        <span @click="getCaptcha">获取验证码</span>
      </label>
    </div>
    <div class="login-link clearfix" v-if="isAccount">
      <span class="change-mode" @click="isAccount = false">短信验证码登录</span>
      <span class="account-register" @click="register">免费注册</span>
    </div>
    <div class="login-link clearfix" v-if="!isAccount">
      <span class="captcha-register" @click="register">免费注册</span>
    </div>
    <div class="login-btn">
      <button class="account-login" @click="login">登录</button>
      <button v-if="!isAccount" @click="isAccount = true" class="valid-login">账号密码登录</button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isAccount: true,
      username: '',
      password: '',
      phone: '',
      captcha: ''
    }
  },
  methods: {
    login () {
      if (this.username === '' || this.password === '') {
        this.$toast.fail('账号密码不能为空!!!')
      } else {
        this.$router.push('/home')
      }
    },
    getCaptcha () {
      console.log('1234')
    },
    register () {
      this.$router.push('/register')
    }
  }
}
</script>

<style scoped lang="less">
  .login {
    padding: 0 20px;
    .header {
      width: 335px;
      height: 120px;
      padding-top: 50px;
      .logo {
        .tb-logo {
          text-align: center;
          img {
            width: 80px;
            height: 80px;
          }
        }
      }
    }
    .form {
      margin-bottom: 20px;
      label:last-child > input {
        margin-top: 40px;
      }
      label {
        position: relative;
        span {
          position: absolute;
          top: 45px;
          left: 250px;
          width: 80px;
          color: #FF5000;
          font-size: 16px;
        }
        input {
          display: block;
          width: 335px;
          height: 31px;
          padding-left: 5px;
          border-bottom: 1px solid #FF5000;
          margin-top: 50px;
          font-size: 16px;
          line-height: 30px;
        }
        input::-webkit-input-placeholder {
          font-size: 16px;
        }
        .clear::after {
          content: '\e700';
        }
        .icon {
          position: absolute;
          font-size: 22px;
          top: 0;
          left: 305px;
        }
      }
    }
    .login-link {
      span {
        font-size: 14px;
        color: #555555;
      }
      .change-mode {
        float: left;
      }
      .account-register {
        float: right;
      }
      .captcha-register {
        float: left;
      }
    }
    .login-btn {
      margin-top: 33px;
      button {
        width: 335px;
        height: 45px;
        font-size: 16px;
        line-height: 45px;
        border-radius: 22.5px;
      }
      .account-login {
        color: white;
        box-shadow: 0 2px 4px #F7C7B1;
        background: -webkit-linear-gradient(left,#FF9000,#FF5000) no-repeat
      }
      .valid-login {
        margin-top: 15px;
        border: 1px solid #FF5000;
        color: #FF5000;
        background: white;
      }
    }
  }
</style>
