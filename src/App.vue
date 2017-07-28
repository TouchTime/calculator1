<template>
  <div id="app">
    <vheader></vheader>
    <input type="text" placeholder="生态系统">
    <router-link to="/goods">商品</router-link>
    <router-link to="/seller">卖家</router-link>
    <router-view></router-view>
  </div>
</template>

<script>
  import vheader from './components/header/header'
export default {
  name: 'app',
  components: {
   vheader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
