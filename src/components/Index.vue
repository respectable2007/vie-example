<template>
  <div class="index">
    <el-head></el-head>
    <el-sidebar></el-sidebar>
    <el-main></el-main>
    <el-footer></el-footer>
    <a href="javascript;:" class="kefu">
      <img src="../assets/kefu.png" alt="在线客服">
    </a>
  </div>
</template>

<script>
import ELHead from './layout/Head.vue'
import ELSidebar from './layout/Sidebar.vue'
import ELMain from './layout/Main.vue'
import ELFooter from './layout/Footer.vue'
export default {
  name: 'index',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    elHead: ELHead,
    elSidebar: ELSidebar,
    elMain: ELMain,
    elFooter: ELFooter
  }
}
</script>

<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
.kefu{
  position: fixed;
  top: 50%;
  margin-top: -40px;
  right: 10px;
}
</style>
