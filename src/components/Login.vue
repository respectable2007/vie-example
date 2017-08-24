<template>
  <div class="login">
    <img src="./../assets/logo.png">
    <el-form ref='form' 
             :model='form'
             :rules='rules'>
             <el-form-item prop='loginName'>
                <el-input v-model='form.loginName'
                          placeholder='请输入用户名'
                          type='text'>
                </el-input>
             </el-form-item>
             <el-form-item prop='loginPwd'>
                <el-input v-model='form.loginPwd'
                          placeholder='请输入密码'
                          :minlength='6'
                          type='password'>
                </el-input>
             </el-form-item>
             <el-form-item prop='loginCode'>
                <el-input v-model='form.loginCode'
                          placeholder="请输入验证码" 
                          type='text'
                          :maxlength='16'>
                  <template slot="append">
                    1234
                    <!-- <img src=''> -->
                  </template>
                </el-input>
             </el-form-item>
             <el-form-item>
                <el-button type='primary'
                           size='large'
                           @click='onSubmit("form")'>
                           登 录
                </el-button>
             </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      form: {
        loginName: '',
        loginPwd: '',
        loginCode: ''
      },
      rules: {
        loginName: [
          {required: true, message: '用户名不可为空', trigger: 'blur'}
        ],
        loginPwd: [
          {required: true, message: '密码不可为空', trigger: 'blur'}
        ],
        loginCode: [
          {required: true, message: '验证码不可为空', trigger: 'blur'}
        ]
      }
    }
  },
  methods: {
    onSubmit (form) {
      this.$refs[form].validate((validate) => {
        if (validate) {
          // 路由导航，相当于router-link
          this.$router.push({name: 'Index'})
        } else {
          return false
        }
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 .login{
  width: 300px;
  margin: 60px auto 0;
 }
 .el-button--large{
  width: 100%;
 }
</style>
