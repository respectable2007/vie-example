<template>
  <div class="main">
    <div class="function layout">
      <div class="mm clearfix">
        <div class="main-sidebar">
          <div >
            <a href="#" 
               class="top">
              我要赚钱
              <i class="el-icon-caret-right"></i>
            </a>
            <div class="title">
              综合理财平台
              <br/>
              坐享稳健收益
            </div>
            <div class="main-img">
            </div>
            <div class="app-list">
              <p>
                丰富理财产品汇聚
              </p>
              <div class="bottom">
                <a href="">
                  挖财宝
                  <i class="el-icon-caret-right"></i>
                </a>
                <span class="weixin">
                  <img src="./../../assets/logo.png">
                  <div class="arrow"></div>
                </span>
              </div>
            </div>
          </div>
        </div>
        <div class="main-content">
          <div class="content-title clearfix">
            <h3 class="color-33">投资理财</h3>
            <a href="#"
               class="color-link">
               我要投资>
            </a>
          </div>
          <div class="content-detail">
            <div class="page">
              <div class="page-container">
               <h2 class="page-title">百万特供—月薪宝尊享版</h2>
               <p class="page-extra">
                  <span>已享0.3%加息</span>
               </p>
               <div class="page-param">
                  <p class="page-info clearfix">
                    <span class="page-content">
                      6
                      <small>.30</small>
                      <span class="divider">-</span>
                      10
                      <small>.30%</small>
                    </span>
                    <span class="page-content-right">30-720天</span>
                  </p>
                  <p class="page-info clearfix">
                     <span>预期年化</span>
                     <span>投资期限</span>
                  </p>
                </div>
              </div>
              <div class="page-container offset">
                <p class="page-info clearfix">
                  <span>起购金额</span>
                  <span>1000000.00元</span>
                </p>
                <p class="page-info clearfix">
                  <span>已购人数</span>
                  <span>91人</span>
                </p>
              </div>
              <div class="page-container offset secure">
                <i class="el-icon-star-off"></i>
                四重保障 安全可靠
              </div>
              <div class="page-btn">
                <a href="#">
                  立即购买
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="jz clearfix">
        <div class="main-sidebar">
          <div >
            <a href="#" 
               class="top">
              我要记账
              <i class="el-icon-caret-right"></i>
            </a>
            <div class="title">
              爱记账•会生活
            </div>
            <div class="main-img">
            </div>
            <div class="app-list">
              <p>
                理性消费，科学理财
              </p>
              <div class="bottom">
                <a href="">
                  挖财记账理财
                  <i class="el-icon-caret-right"></i>
                </a>
                <span class="weixin">
                  <img src="./../../assets/logo.png">
                  <div class="arrow"></div>
                </span>
              </div>
            </div>
          </div>
        </div>
        <div class="main-content">
            <div class="jz-default">
              <p class="jz-mask"></p>
              <h3>记录每一笔账，管好每一分钱</h3>
              <p>
                爱记账
                <span>•</span> 
                会生活
              </p>
              <a href="">开始记账</a>
            </div>
        </div>
      </div>
      <div class="gq clearfix">
        <div class="main-sidebar">
          <div >
            <a href="#" 
               class="top">
              我要管钱
              <i class="el-icon-caret-right"></i>
            </a>
            <div class="title">
              让投资赚钱更简单
            </div>
            <div class="main-img">
            </div>
            <div class="app-list">
              <p>
                预测风险，提升收益
              </p>
              <div class="bottom">
                <a href="">
                  挖财钱管家
                  <i class="el-icon-caret-right"></i>
                </a>
                <span class="weixin">
                  <img src="./../../assets/logo.png">
                  <div class="arrow"></div>
                </span>
              </div>
            </div>
          </div>
        </div>
        <div class="main-content">
        <div class="content-title clearfix">
            <h3 class="color-33">投资管理</h3>
          </div>
          <div class="content-detail">
            <div class="page">
              <div class="sy">
                <div class="sy-img">
                  <img src="../../assets/gq_back.png">
                </div>
                <div class="sy-img-zoom" 
                     :style='{top:zoomTop+"px",backgroundPositionY:zoomY+"px"}'>
                </div>
                <div class="sy-img-hover"
                     @mousemove.self='scrollImg'>
                </div>
              </div>
              <h3>你算得清收益吗？</h3>
              <p>
                支持股票、基金、银行、网络
                <br/>
                理财等产品收益查看
              </p>
            </div>
            <div class="page">
              <div class="sy">
                <div class="zq-img"
                     :class='zqHover'
                     @mouseenter='scrollZq'
                     @mouseout='scrollZqNo'>
                </div>
              </div>
              <h3>你知道买什么最赚钱吗？</h3>
              <p>
                轻松了解自己的投资分布
                <br/>
                赚钱心中有数
              </p>
            </div>
            <div class="page">
              <div class="sy">
                <div class="tz-img"
                     @mouseenter.self='showHigh'
                     @mouseout='hideHigh'>
                  <canvas id='myCanvas' 
                          width="200" 
                          height="200">
                  </canvas>
                  <p class="tz-img-word"
                     v-show='isShow'>偏高</p>
                  <p class="tz-img-word"
                     v-show='!isShow'>适中</p>
                </div>
                <div class="tz-hove"></div>
              </div>
              <h3>你的投资方法正确吗？</h3>
              <p>
                每时每刻都可查阅资产优化点
                <br/>
                遵循建议、提高收益
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div ></div>
    <div ></div>
  </div>
</template>

<script>
export default {
  mounted () {
    let c = document.getElementById('myCanvas')
    let cxt = c.getContext('2d')
    this.canvas = cxt
    this.hideHigh()
  },
  data () {
    return {
      zoomTop: 0,
      zoomY: 0,
      zqHover: null,
      interval: null,
      isShow: true,
      canvas: null
    }
  },
  methods: {
    scrollImg () {
      if ((event.offsetY - 50) <= 0) {
        this.zoomTop = 0
      } else if ((event.offsetY - 50) >= 90) {
        this.zoomTop = 90
      } else {
        this.zoomTop = event.offsetY - 50
      }
      this.zoomY = -event.offsetY
    },
    scrollZq () {
      let obj = 2
      let that = this
      this.interval = setInterval(() => {
        switch (obj) {
          case 2:
            that.zqHover = {zqImg2: true}
            break
          case 4:
            that.zqHover = {zqImg4: true}
            break
          case 6:
            that.zqHover = {zqImg6: true}
            break
          case 8:
            that.zqHover = {zqImg8: true}
            break
        }
        obj = obj + 2
      }, 120)
    },
    scrollZqNo () {
      this.zqHover = null
      clearInterval(this.interval)
    },
    showHigh () {
      this.isShow = false
      let cxt = this.canvas
      cxt.clearRect(0, 0, 800, 800)
      for (let i = 0; i < 5; i++) {
        cxt.beginPath()
        cxt.lineWidth = 2
        cxt.moveTo(100 + 80 * Math.cos((i * 72) / 180 * Math.PI), 100 + 80 * Math.sin((i * 72) / 180 * Math.PI))
        cxt.lineTo(100 + 80 * Math.cos(((i + 1) * 72) / 180 * Math.PI), 100 + 80 * Math.sin(((i + 1) * 72) / 180 * Math.PI))
        cxt.strokeStyle = 'rgb(54,138,242)'
        cxt.stroke()
        cxt.fill()
      }
      for (let i = 0; i < 5; i++) {
        cxt.beginPath()
        cxt.lineWidth = 2
        cxt.arc(100 + 80 * Math.cos((i * 72) / 180 * Math.PI), 100 + 80 * Math.sin((i * 72) / 180 * Math.PI), 2, 0, 2 * Math.PI, false)
        cxt.strokeStyle = 'rgb(54,138,242)'
        cxt.fillStyle = '#fff'
        cxt.stroke()
        cxt.fill()
      }
    },
    hideHigh () {
      this.isShow = true
      let cxt = this.canvas
      cxt.clearRect(0, 0, 800, 800)
      let coors = [
      [100 + 60 * Math.cos((0 * 72) / 180 * Math.PI), 80 + 50 * Math.sin((0 * 72) / 180 * Math.PI)],
       [100 + 90 * Math.cos((1 * 72) / 180 * Math.PI), 100 + 40 * Math.sin((1 * 72) / 180 * Math.PI)],
        [100 + 46 * Math.cos((2 * 72) / 180 * Math.PI), 100 + 82 * Math.sin((2 * 72) / 180 * Math.PI)],
         [100 + 70 * Math.cos((3 * 72) / 180 * Math.PI), 100 + 40 * Math.sin((3 * 72) / 180 * Math.PI)],
          [100 + 4 * Math.cos((4 * 72) / 180 * Math.PI), 100 + 82 * Math.sin((4 * 72) / 180 * Math.PI)]]
      cxt.beginPath()
      cxt.lineWidth = 2
      for (let i = 0; i < coors.length; i++) {
        cxt.moveTo(coors[i][0], coors[i][1])
        if (i !== 4) {
          cxt.lineTo(coors[i + 1][0], coors[i + 1][1])
        } else {
          cxt.lineTo(coors[0][0], coors[0][1])
        }
      }
      cxt.strokeStyle = 'rgb(54,138,242)'
      cxt.stroke()
      cxt.fillStyle = 'rgb(54,138,242)'
      cxt.fill()
      cxt.closePath()
      for (let i = 0; i < coors.length; i++) {
        cxt.beginPath()
        cxt.lineWidth = 2
        cxt.arc(coors[i][0], coors[i][1], 2, 0, 2 * Math.PI, false)
        cxt.strokeStyle = 'rgb(54,138,242)'
        if (i % 2) {
          cxt.strokeStyle = 'red'
          cxt.fillStyle = 'red'
        } else {
          cxt.fillStyle = '#fff'
        }
        cxt.stroke()
        cxt.fill()
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.function > div{
  padding: 30px 0;
  border-bottom: 1px solid #e7e7e7;
  position: relative;
}
.function > div:last-child{
  border-bottom: none;
}
 .main-sidebar{
  position: relative;
  float: left;
  margin-right: 6px;
  height: 363px;
  width: 144px;
  background: #fa5546;
  padding: 9px 20px 8px 20px;
 }
 .main-sidebar:after{
  content: '';
  background: #fa5546;
  opacity: 0.4;
  position: absolute;
  top: 5px;
  bottom: 5px;
  right: -6px;
  width: 6px;
 }
 .top{
  color: #fff;
  font-size: 22px;
  font-weight: bold;
 }
 .top i{
  margin-left: 26px;
 }
 .title{
  text-align: left;
  margin-top: 10px;
  color: #fff;
  font-weight: bold;
 }
 .main-img{
  height: 76px;
  width: 89px;
  margin: 60px 0 80px 30px;
  background: url('./../../assets/fun_bar.png') no-repeat;
  background-position: -11px -9px;
 }
 .app-list p{
  text-align: left;
  color: #c44338;
  font-weight: bold;
  margin-bottom: 6px; 
 }
 .app-list a{
  background: #fff;
  border-radius: 3px;
  color: red;
  display: block;
  padding: 8px 30px 8px 0;
  position: relative;
 }
 .app-list a i{
    position: absolute;
    height: 100%;
    right: 0;
    top: 0;
    width: 34px;
    border-left: 1px solid #e7e7e7;
    line-height: 34px;
 }
 .app-list a:hover{
  background: rgba(0,0,0,0.2);
  color: #fff;
 }
 .app-list .bottom{
  position: relative;
 }
 .app-list a:hover > i{
  border-left: 1px solid rgba(255,255,255,0.2);
 }
 .app-list a:hover+.weixin{
  display: block;
 }
 .app-list .bottom .weixin{
  display: none;
  position: absolute;
  background: #fff;
  padding: 4px;
  border-radius: 3px;
  border: 4px solid rgba(0,0,0,0.5);
  top: -80px;
  left: 154px;
  z-index: 10;
 }
 .weixin .arrow{
  width: 0;
  height: 0;
  position: absolute;
  top: 39%;
  left: -13px;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-right: 10px solid rgba(0,0,0,0.5);
 }
 .main-content{
  float:left;
  width: 810px;
 }
 .main-content .content-title{
  padding-left: 26px;
 }
 .content-title h3{
  float: left;
  font-size: 20px;
  font-weight: 400;
  margin: 0;
  padding:0;
 }
 .content-title a{
  float: right;
  line-height: 38px;
  color: 
 }
 .content-detail .page{
  float:left;
  width: 210px;
  padding: 10px 29px 0 30px;
  height: 340px;
  border-right: 1px solid #e7e7e7;
 }
 .content-detail .page:last-child{
  border-right: none;
 }
 .content-detail .page .page-container{
  border-bottom: 1px dotted #e7e7e7;
 }
 .content-detail .page .page-container h2{
  font-weight: 400;
  margin: 10px 0 6px 0;
 }
 .content-detail .page .page-container .page-extra span{
  background: #ff9128;
  font-weight: bold;
  color: #fff;
  padding: 0 2px;
 }
 .page-param{
  margin: 20px 0;
 }
 .page-param .page-content{
  color: red;
  font-size: 24px;
  font-weight: normal;
 }
 .page-param .page-content small{
  font-size: 14px;
  margin-left: -8px;
 }
 .page-info .page-content-right{
  font-size: 18px;
  padding-top: 7px;
  color: #000;
  font-weight: normal;
 }
 .page-info .divider{
  margin: 0 -6px;
  color: red;
 }
 .page-info span{
  color: #999;
  font-weight: bold;
 }
 .page-info span:first-child{
  float: left;
 }
 .page-info span:last-child{
  float: right;
 }
 .page-container.offset p{
  line-height: 28px;
 }
 .secure{
  color: #62b7f1;
  font-weight: bold;
 }
 .page .page-btn a{
  display: block;
  width: 116px;
  height: 34px;
  line-height: 34px;
  font-size: 16px;
  color: red;
  border: 1px solid red;
  border-radius: 3px;
  margin: 20px auto;
 }
 .jz .main-sidebar{
  background: #3ab28c;
 }
 .jz .main-sidebar:after{
  background: #3ab28c;
 }
 .jz .main-img{
    height: 102px;
    width: 102px;
    margin: 60px 0 70px 20px;
    background-position: -207px -9px;
 }
 .jz .app-list p{
  color: #197d5f;
 }
 .jz .app-list a{
  color: #3ab28c;
 }
 .jz .app-list a:hover{
  color: #fff;
 }
 .jz .jz-default{
  width: 100%;
  height: 380px;
  background: url('./../../assets/ji_back.png') no-repeat;
  position: relative;
 }
 .jz .jz-default .jz-mask{
  position: absolute;
  width: 100%;
  height: 100%;
  background: #fff;
  opacity: 0.9;
 }
 .jz .jz-default h3{
  position: relative;;
  font-size: 34px;
  color: #000;
  margin: 0;
  padding-top: 66px;
 }
 .jz .jz-default p{
  position: relative;
  font-size: 18px;
  color: #000;
  padding-top: 26px;
 }

 .jz .jz-default a{
  position: relative;
  display: block;
  width: 116px;
  height: 34px;
  line-height: 34px;
  margin:0 auto;
  margin-top: 100px;
  border: 1px solid green;
  color: green;
  border-radius: 3px;
  font-size: 16px;
 }
 .gq .main-sidebar{
  background: #4c9aea;
 }
 .gq .main-sidebar:after{
  background: #4c9aea;
 }
 .gq .main-img{
    height: 112px;
    width: 112px;
    margin: 60px 0 70px 20px;
    background-position: -653px -9px;
 }
 .gq .app-list p{
  color: #1974b0;
 }
 .gq .app-list a{
  color: #319ae0;
 }
 .gq .app-list a:hover{
  color: #fff;
 }
 .gq .content-detail h3{
  font-size: 18px;
 }
 .gq .content-detail p{
  color: #b5b9be;
 }
 .gq .page:first-child{
  padding-left: 10px;
  width: 240px;
  padding-right: 20px;
 }
 .gq .sy{
  position: relative;
 }
 .gq .sy-img {
  text-align: right;
 }
 .gq .sy-img img{
  width: 120px;
 }
 .gq .sy-img-zoom{
  position: absolute;
  width: 225px;
  height: 100px;
  border-radius: 3px;
  border: 1px solid gray;
  bottom: 0;
  background-position-x:0;
  background-image: url('./../../assets/gq_back.png');
  background-repeat: no-repeat;
  background-size: 225px 365.7px;
 }
 .gq .sy-img-hover{
  position: absolute;
  background: red;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0;
  cursor:pointer;
 }
 .gq .zq-img{
  background-image: url('./../../assets/gq_zq.png');
  height: 156px;
  background-repeat: no-repeat;
  background-size: 156px 2526px;
  margin: 31px 0 31px 24px;
 }
 .gq .zq-img.zqImg2{
  background-position: 0 -790px;
 }
 .gq .zq-img.zqImg4{
  background-position: 0 -1264px;
 }
 .gq .zq-img.zqImg6{
  background-position: 0 -1896px;
 }
 .gq .zq-img.zqImg8{
  background-position: 0 -2370px;
 }
 .gq .tz-img{
  background-image: url('./../../assets/rate.png');
  height: 200px;
  background-repeat: no-repeat;
  background-size: 200px 200px;
  margin: 0 7px 0 7px;
  position: relative;
  cursor: pointer;
 }
 .gq .tz-img .tz-img-word{
    position: absolute;
    top: 50%;
    margin-top: -16px;
    left: 50%;
    margin-left: -20px;
    color:#333;
    font-size: 22px;
    font-weight: bold;
 }
</style>
