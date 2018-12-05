<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
  <!-- 前路由地址所对应的内容，router中index.js中找 -->
    <keep-alive>
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
}
</style>
