<template>
  <div id="app">
    <!-- 除了Detail都会被缓存 
        导致详情页下滑隐藏的header不出现
    -->
    <keep-alive exclude="Detail">
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
</style>
