<template>
  <div class="register-container">
    <header>
      <div class="title">手机号注册</div>
      <div class="sub-title">亲，欢迎注册淘宝账号</div>
    </header>
    <div class="register-form">
      <div class="form phone">
        <div class="phone-prefix">
          <span>+86</span>
        </div>
        <div class="phone-input"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  data () {
    return {}
  }
}
</script>

<style scoped lang="less">
  .register-container {
    margin-top: 65px;
    padding: 0 27px;
    header {
      .title {
        font-size: 30px;
        color: #333333;
        font-weight: 400;
        line-height: 1.15;
      }
      .sub-title {
        margin-top: 12px;
        font-size: 16px;
        color: #999999;
        font-weight: 400;
        line-height: 1.15;
      }
    }
    .register-form {
      margin-top: 50px;
      .form {
        width: 320px;
        padding-left: 15px;
        border-bottom: 1px solid #CCCCCC;
      }
      .phone {
        .phone-prefix {
          position: relative;
          span {
            display: inline-block;
            padding: 7px 0;
            font-size: 16px;
            color: #000000;
            font-family: PingFangSC-Light,sans-serif;
          }
          :after {
            position: absolute;
            content: '\e783';
            font-size: 14px;
            font-family: iconfont;
            left: 35px;
            font-weight: 700;
          }
        }
      }
    }
  }
</style>
