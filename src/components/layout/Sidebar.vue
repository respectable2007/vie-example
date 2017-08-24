<template>
  <div class="sidebar">
    <div class="mainbar clearfix">
      <div class="mainbar-left">
        <h1 class="logo">
        </h1>
        <div class="bar">
          <ul class="bar-menu">
            <li>
              <a href="#">首页</a>
            </li>
            <li class="bar-menu-sublist">
              <a href="#">我要赚钱
                <i class="el-icon-caret-bottom"></i>
                <div class="bar-menu-container">
                  <ul>
                    <li>
                      <a href="#">投资理财</a>
                    </li>
                    <li>
                      <a href="#">我的理财</a>
                    </li>
                  </ul>
                </div>
              </a>
            </li>
            <li>
              <a href="#">钱堂社区</a>
            </li>
            <li>
              <a href="#">我的挖财</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="mainbar-right">
        <a href="#">登录</a>
        <a href="#">新用户注册</a>
      </div>
    </div>
    <div class="adbar"
         :class="hoverBack"
         @click.self='barJump'>
      <div class="bar-btn clearfix">
        <a href="javascript;:" 
           v-for='index in 5'
           :class='{select:id==index}'
           @mouseenter='backHove(index)'
           @mouseout='outHover'>
        </a>
      </div>
    </div>
    <div class="tipbar">
      <ul class="layout clearfix">
        <li >
          <i class="tip-img tip-img-1"></i>
          <p class="tip-title">8年积淀</p>
          <p>1.6亿用户的选择</p>
        </li>
        <li>
          <i class="tip-img tip-img-2"></i>
          <p class="tip-title">7X24小时</p>
          <p>您随时的资产管家</p>
        </li>
        <li>
          <i class="tip-img tip-img-3"></i>
          <p class="tip-title">三重十道</p>
          <p>全面的风控管理策略</p>
        </li>
        <li>
          <i class="tip-img tip-img-4"></i>
          <p class="tip-title">2亿美元融资</p>
          <p>领先的在线金融专家</p>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  computed: {
    hoverBack () {
      return 'step' + this.id
    }
  },
  data () {
    return {
      id: 1,
      intervalid: null
    }
  },
  methods: {
    backHove (index) {
      clearInterval(this.intervalid)
      switch (index) {
        case 1:
          this.id = 1
          break
        case 2:
          this.id = 2
          break
        case 3:
          this.id = 3
          break
        case 4:
          this.id = 4
          break
        case 5:
          this.id = 5
          break
      }
    },
    barJump () {
      alert(this.hoverBack)
    },
    outHover () {
      this.addInterval()
    },
    addInterval () {
      let that = this
      that.intervalid = setInterval(() => {
        that.id ++
        if (that.id > 5) {
          that.id = 1
        }
      }, 3000)
    }
  },
  created () {
    this.addInterval()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 .mainbar{
  width: 1000px;
  margin: 0 auto;
  text-align: left;
  padding: 20px 0;
  height: 34px;
 }
 .mainbar-left h1,.mainbar-left div,.bar .bar-menu li{
  display: inline-block;
 }
 .bar{
  margin-left: 68px;
  line-height: 34px;
 }
 .bar .bar-menu li a{
  display: block;
  height: 100%;
  font-size: 15px;
  color: #666;
  padding: 0 16px;
 }
 .bar .bar-menu li a:hover{
  color: red;
 }
 .bar .bar-menu li a:hover i{
  color: #666;
 }
 .bar-menu-sublist i{
  font-size: 12px;
 }
 .mainbar-left{
  float: left;
 }
 .bar-menu-sublist a{
  position: relative;
 }
 .bar-menu-sublist .bar-menu-container{
  position: absolute;
  left: -2px;
  width: 100%;
  display: none;
  z-index: 100;
  background: #fff;
 }
 .bar-menu-sublist a:hover .bar-menu-container{
  display: block;
 }
 .bar-menu-sublist .bar-menu-container ul{
  border:1px solid #e7e7e7;
  border-radius: 4px;
  padding: 2px 0;
 }
 .bar-menu .bar-menu-sublist ul li{
  display: block;
 }
 .bar-menu .bar-menu-sublist ul li a{
  display: block;
  width: 100%;
  padding: 0;
  text-align: center;
 }
 .bar-menu .bar-menu-sublist ul li a:hover{
  background: #eee;
 }
 .logo{
   width: 34px;
   height: 34px;
   position: absolute;
   background-image: url('./../../assets/logo.png');
   background-position: 0 -12px;
 }
 .mainbar-right{
  float: right;
  height: 100%;
  line-height: 100%;
  font-size: 14px;
 }
 .mainbar-right a{
  display: inline-block;
  height: 100%;
  line-height: 34px;
 }
 .mainbar-right a:first-child{
  color:red;
  margin-right: 10px;
 }
 .mainbar-right a:last-child{
  border:1px solid red;
  width: 88px;
  border-radius: 3px;
  text-align: center;
  color:red;
 }
 .mainbar-right a:last-child:hover{
  background: red;
  color: #fff;
  font-weight: bold;
 }
 .adbar{
  height: 280px;
  background: red;
  width: 100%;
  position: relative;
 }
 .bar-btn{
  position: absolute;
  width: 200px;
  height: 8px;
  margin-left: -100px;
  left: 50%;
  bottom: 30px;
 }
 .bar-btn a{
  float: left;
  background: rgba(255,255,255,0.4);
  width: 28px;
  margin:0 6px;
  height: 100%;
  cursor: default;
 }
 .bar-btn a:hover{
  background: rgb(255,255,255);
 }
 .bar-btn a.select{
  background: rgb(255,255,255);
 }
 .step1{
  background-image: url('./../../assets/1.png');
  background-repeat: no-repeat;
  background-position: 170px;
  background-color: rgb(110,33,182);
  cursor: pointer;
 }
 .step2{
  background-image: url('./../../assets/2.jpg');
  background-repeat: no-repeat;
  background-position: 170px;
  background-color: rgb(255,240,175);
  cursor: pointer;
 }
 .step3{
  background-image: url('./../../assets/3.jpg');
  background-repeat: no-repeat;
  background-position: 170px;
  background-color: rgb(34,22,63);
  cursor: pointer;
 }
 .step4{
  background-image: url('./../../assets/4.png');
  background-repeat: no-repeat;
  background-position: 170px;
  background-color: rgb(23,25,42);
  cursor: pointer;
 }
 .step5{
  background-image: url('./../../assets/5.jpg');
  background-repeat: no-repeat;
  background-position: 170px;
  background-color: rgb(22,176,246);
  cursor: pointer;
 }
 .tipbar{
  height: 55px;
  background: #f7f7f7;
  padding-top: 15px;
  color: #aba7a2;
 }
 .tipbar ul li{
  float: left;
  width: 25%;
 }
 .tip-img{
   float: left;
   width: 40px;
   height: 40px;
   margin-right: 20px;
   background-image: url('./../../assets/tip_bar.png');
   background-repeat: no-repeat;
 }
 .tip-img-1{
  background-position:-11px -90px;
 }
 .tip-img-2{
  background-position:-71px -90px;
 }
 .tip-img-3{
  background-position:-131px -90px;
 }
 .tip-img-4{
  background-position:-191px -90px;
 }
 .tip-layout li p{
  text-align: left;
  font-weight: bold;
 }
 .tip-title{
  font-size: 16px;
  color: #66625e;
 }
</style>
