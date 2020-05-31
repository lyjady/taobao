<template>
  <div class="login">
    <header class="header">
      <div class="logo">
        <div class="tb-logo">
          <img src="../static/image/login-logo.png" alt="...">
        </div>
      </div>
    </header>
    <div class="form">
      <label>
        <input class="clear" type="text" placeholder="手机号/邮箱/会员名">
      </label>
      <label>
        <input class="clear" type="password" placeholder="请输入登录密码">
      </label>
    </div>
    <div class="login-link clearfix">
      <span>短信验证码登录</span>
      <span>免费注册</span>
    </div>
    <div class="login-btn">
      <button>登录</button>
    </div>
  </div>
</template>

<script>
export default {
  name: ''
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

      span:first-child {
        float: left;
      }

      span:last-child {
        float: right;
      }
    }
    .login-btn {
      margin-top: 33px;
      button {
        width: 335px;
        height: 45px;
        color: white;
        border-radius: 22.5px;
        font-size: 16px;
        box-shadow: 0 2px 4px #F7C7B1;
        line-height: 45px;
        background: -webkit-linear-gradient(left,#ff9000,#ff5000) no-repeat
      }
    }
  }
</style>
