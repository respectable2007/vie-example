<template>
  <div class="footer">
    <div class="footer-contact">
      <div class="footer-logo">
        <img src="../../assets/wacai.png">
      </div>
      <div class="footer-detail">
        <p>
          客服热线：（周一至周五 9:00-18:00）
        </p>
        <p class="strong">
          400-711-8718
        </p>
        <p>
          客服电话：0571-56967116
        </p>
        <p>
          在线客服：点此茶香
        </p>
        <p>
          客服邮箱：kf@wacai.com
        </p>
      </div>
      <div class="footer-other">
      <img src="../../assets/wac_code.png">
      微信扫一扫
      <a href="" class="weibo">官方微博</a>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="footer-contact">
        <p class="ft-link">
          <a href="">关于挖财</a> |
          <a href="">诚聘英才</a> |
          <a href="">联系我们</a> |
          <a href="">常见问题</a> |
          <a href="">友情链接</a> |
          <a href="">网站地图</a>
        </p>
        <div class="ft-right">
          <p>
            杭州挖财互联网金融服务有限公司版权所有 2009-2017 浙ICP备09103445<br/>
            增值电信业务经营许可证浙B2-20140363<br/>
            理财市场有风险，投资需谨慎
          </p>
          <div class="ft-other">
            <a href="" class="norton"></a>
            <a href="http://www.pingpinganan.gov.cn" class="safe"></a>
          </div>
      </div>
      </div>
    </div>
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
 .footer{
  margin: 0 auto;
  height: 313px;
  background: #252525;
 }
 .footer-contact{
  width: 1000px;
  margin:0 auto;
  height: 215px;
  position: relative;
 }
 .footer-logo{
  position: absolute;
  top: 50%;
  margin-top: -27px;
 }
 .footer-detail{
  position: absolute;
  left: 172px;
  top: 50%;
  margin-top: -71px;
  color: #818181;
  text-align: left;
 }
 .footer-detail p{
  margin-bottom: 8px;
 }
 .footer-detail p.strong{
  font-size: 20px;
  font-weight: 700;
 }
 .footer-other{
  position: absolute;
  right: 0;
  top: 50%;
  margin-top: -50px;
  color: #818181;
 }
 .footer-other img{
  vertical-align: middle;
  margin-right: 20px;
 }
 .footer-other .weibo{
  margin-left: 40px;
  color: #818181;
 }
 .footer-other .weibo:hover{
  color: #808080;
 }
 .footer-bottom{
  background: #1b1b1b;
  height: 98px;
 }
 .footer-bottom .footer-contact{
  height: 100%;
  text-align: left;
 }
 .ft-link{
  line-height: 98px;
  color: #818181;
 }
 .ft-link a{
  color: #818181;
 }
 .ft-right{
    position: absolute;
    top: 0;
    text-align: right;
    right: 0;
    color: #818181;
 }
 .ft-right .ft-other{
  height: 36px;
  line-height: 36px;
 }
 .ft-other a{
  display: inline-block;
  height: 26px;
 }
 a.norton{
  background-image:url('./../../assets/gongan.jpg');
  width: 94px;
  background-repeat: no-repeat;
 }
 a.safe{
  background-image:url('./../../assets/gongan_b.jpg');
  width: 94px;
  background-repeat: no-repeat;
 }
</style>
