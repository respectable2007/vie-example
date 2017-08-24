<template>
  <div class="head">
    <div class="head-content clearfix">
      <div class="head-left">
        <a href="javascirpt:;">收藏本站</a>
      </div>
      <div class="head-right">
        <ul>
          <li>
            <a href="javascirpt:;" class="home">
              <i class="el-icon-setting"></i>
              挖财
            </a>
          </li>
          <li>
            <a href="">
              挖财宝
            </a>
          </li>
          <li>
            <a href="">
              信用卡
            </a>
          </li>
          <li class="sub-menu">
            <a href="javascirpt:;">
              应用下载
              <i class="el-icon-caret-bottom"></i>
              <div class="sub-menu-container">
                <ul class="sub-menu-list">
                  <li>
                    <a href="javascirpt:;">
                      <i class="el-icon-date min-logo"></i>
                      <strong class="icon-title">
                        记账理财
                      </strong>
                      <p class="icon-tip">
                        记账
                        <span>•</span>
                        管理
                        <span>•</span>
                        理财
                        &emsp; 
                        <strong>
                          一亿人的选择
                        </strong>
                      </p>
                    </a>
                  </li>
                  <li>
                    <a href="javascirpt:;">
                      <i class="el-icon-date min-logo"></i>
                      <strong class="icon-title">
                        挖财宝
                      </strong>
                      <p class="icon-tip">
                        安全
                        <span>•</span>
                        方便
                        <span>•</span>
                        优质收益
                        &emsp; 
                        <strong>
                          理财神器
                        </strong>
                      </p>
                    </a>
                  </li>
                  <li>
                    <a href="javascirpt:;">
                      <i class="el-icon-date min-logo"></i>
                      <strong class="icon-title">
                        挖财钱管家
                      </strong>
                      <p class="icon-tip">
                        全资产管理
                        <span>•</span>
                        资产体检
                        <span>•</span>
                        投资顾问
                      </p>
                    </a>
                  </li>
                  <li>
                    <a href="javascirpt:;">
                      <i class="el-icon-date min-logo"></i>
                      <strong class="icon-title">
                        信用卡管家
                      </strong>
                      <p class="icon-tip">
                        管卡还款
                        <span>•</span>
                        办卡提额
                        <span>•</span>
                        信用增值
                      </p>
                    </a>
                  </li>
                  <li>
                    <a href="javascirpt:;">
                      <i class="el-icon-date min-logo"></i>
                      <strong class="icon-title">
                        钱堂社区
                      </strong>
                      <p class="icon-tip">
                        有人
                        <span>•</span>
                        有钱
                        <span>•</span>
                        有故事
                        &emsp; 
                        <strong>
                          理财社区
                        </strong>
                      </p>
                    </a>
                  </li>
                  <li>
                    <a href="javascirpt:;">
                      <i class="el-icon-date min-logo"></i>
                      <strong class="icon-title">
                        挖财股神
                      </strong>
                      <p class="icon-tip">
                        模拟炒股赚真钱
                        <span>•</span>
                        <strong>
                          赚了可提现
                        </strong>
                      </p>
                    </a>
                  </li>
               </ul>
             </div>
            </a>
          </li>
          <li>
            <a href="#">
              钱堂社区
            </a>
          </li>
          <li>
            <a href="#">
              帮助中心
            </a>
          </li>
        </ul>
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
 .head{
  height: 30px;
  background: #f2f2f2;
  line-height: 30px;
 }
 .head-content{
  margin: 0 auto;
  width: 1000px;
 }
 .head-left{
  float: left;
 }
 .head-right{
  float: right;
 }
 .head-right ul li{
  display: inline-block;
  position: relative;
  margin-left: 20px;
 }
 a{
  color: #999;
  font-weight: bold;
  width: 100%;
  height: 100%;
  display: block;
 }
 a:hover{
  text-decoration: underline;
 }
 .sub-menu ul{
  position: absolute;
  width: 287px;
  border:1px solid #999;
  border-radius: 4px;
  left: -105px;
  padding:10px 0;
  z-index: 1001;
  background: #fff;
 }
 .sub-menu ul li{
  margin-left: 0;
  width: 100%;
  padding: 0;
 }
 .sub-menu ul li a{
  display: block;
  width: 100%;
  padding: 12px 0;
  line-height: 22px;
  text-align: left;
 }
 .sub-menu ul li a:hover{
  background: #eee;
 }
 .sub-menu ul li a .min-logo{
  float: left;
  width: 40px;
  height: 40px;
  margin:0 12px;
  font-size: 44px;
 }
 .sub-menu a:first-child:hover .sub-menu-container{
  display: block;
  opacity: 1;
 }
 .sub-menu-container{
  padding-top: 4px;
  display: none;
  opacity:0; 
  transition:all 1s;
  z-index: 100;
 }
 .sub-menu-container a:hover{
  text-decoration: none;
 }
 .icon-title{
  font-weight: bold;
  font-size: 16px;
  color: #333;
 }
 .icon-tip{
  font-weight: 700;
  font-size: 13px;
 }
</style>
