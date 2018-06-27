<template>
  <el-container class="container-wrapper">
    <el-header><top-bar></top-bar></el-header>
    <el-container><el-main><router-view></router-view></el-main></el-container>
    <el-footer><foot-bar></foot-bar></el-footer>
  </el-container>
</template>

<script>
import TopBar from 'components/top-bar';
import FootBar from 'components/foot-bar';
export default {
  name: 'static-layout',
  components: {
    'top-bar': TopBar,
    'foot-bar': FootBar
  }
};
</script>
<style lang="scss" scoped>
</style>
