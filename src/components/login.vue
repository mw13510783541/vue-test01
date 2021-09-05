<template>
  <div class="login_content">
    <div class="login_form">
      <div class="img_up">
        <img src="../assets/logo.png" alt />
      </div>
      <!-- 表单区域 -->
      <el-form ref="form" :model="form" label-width="0px" class="form_box">
        <el-form-item>
          <el-input v-model="form.name" placeholder="用户名"></el-input>
        </el-form-item>
        <el-form-item>
          <el-input v-model="form.password" placeholder="密码"></el-input>
        </el-form-item>
        <el-form-item class="btn_group">
          <el-button type="primary">确定</el-button>
          <el-button type="info">重置</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      form: {
          name: '',
          password: '',
          region: '',
      }
    }
  },
}
</script>

<style lang="less" scoped>
.login_content {
  width: 100%;
  height: 100%;
  background-color: #3f71b5;
  position: relative;
  .login_form {
    width: 450px;
    height: 300px;
    background-color: #fff;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border-radius: 3px;
    .img_up {
      width: 130px;
      height: 130px;
      border: 1px solid #ccc;
      position: absolute;
      left: 50%;
      transform: translate(-50%, -50%);
      border-radius: 50%;
      background-color: #fff;
      overflow: hidden;
      padding: 10px;
      box-shadow: 0 0 10px #ddd;
      img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
        background-color: #eee;
      }
    }
    .form_box {
      margin-top: 80px;
      padding: 10px;
      .btn_group {
        display: flex;
        justify-content: center
      }
    }
  }
}
</style>