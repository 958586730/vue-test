<template>
  <div class="card">
    <div class="user-card">
      <el-form class="form" ref="form" :model="form" label-width="80px" label-position="top">
        <el-form-item label="用户">
          <el-input placeholder="请输入用户" clearable v-model="dataForm.user"></el-input>
        </el-form-item>
        <el-form-item label="密码">
          <el-input placeholder="请输入用户" clearable v-model="dataForm.password"></el-input>
        </el-form-item>
        <el-form-item label="验证码">
          <div class="verification_div">
            <div class="verification_input">
              <el-input placeholder="请输入用户" clearable v-model="dataForm.yan"></el-input>
            </div>
            <div class="verification_button">
              <el-button type="success">获取验证码</el-button>
            </div>
          </div>
        </el-form-item>
        <el-form-item>
          <div class="submit">提交</div>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      dataForm: {
        user: '',
        password: '',
        yan: ''
      }
    }
  },
  methods: {
    onSubmit () {
      console.log('submit!');
    }
  }
}
</script>
<style>
.form .el-form-item__label {
  color: aliceblue !important;
}
</style>
<style lang="scss" scoped>
.card {
  height: 100vh;
  background-color: #334960;
}
.user-card {
  padding: 10vh 80vh 0vh 80vh;
}
.verification_div {
  display: flex;
}
.verification_input {
  margin-right: 60px;
}
.submit {
  border: 1px solid #ff9487;
  background-color: #ff9487;
  text-align: center;
  border-radius: 4px;
  color: aliceblue;
}
.verification_button {
  float: right;
}
</style>