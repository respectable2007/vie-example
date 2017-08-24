<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font:12px/1.5 PingFang SC,Microsoft YaHei,Helvetica,Arial,sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
html,body{
  height: 100%;
}
body,div,a,ul,li,ol,p,strong,h1{
  margin: 0;
  padding: 0;
}
li{
  list-style: none;
}
a{
 text-decoration: none;
}
strong{
  margin: 0;
  padding: 0;
  border: 0;
  outline: 0;
  font-size: 100%;
  vertical-align: baseline;
  background: transparent;
}
.clearfix:after{
  content: '.';
  display: block;
  height: 0;
  clear: both;
  visibility: hidden;
}
.layout{
  width: 1000px;
  margin:0 auto;
 }
 .color-33{
  color: #333;
 }
 .color-link{
  color: #666;
 }
 .offset{
  padding: 10px 0;
 }
</style>
