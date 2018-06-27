<!-- 顶部导航组件 -->
<!-- 使用说明：<top-bar></top-bar> -->
<template>
    <div id="footbar-wrap">
        <el-row type="flex" justify="space-between">
            <el-col :span="12">
                <a href="/index.html">联系我们</a>
                <a href="/products.html">招聘专区</a>
            </el-col>
        </el-row>
    </div>
</template>
<script>
export default {
  name: 'foot-bar',
  data () {
    return {
    };
  },
  computed: {
  },
  methods: {
  }
};
</script>
<style scoped lang="scss">
#footbar-wrap {
  overflow: hidden;
  border-bottom: 1px solid #e7eaec;
  background: #324157;
  color: #fff;
  padding: 0 15px;
  z-index: 4;
  box-sizing: border-box;
  transition: all 0.3s;
  .logo {
    color: #fff;
    font-weight: bold;
    line-height: 60px;
    margin: 0;
    letter-spacing: 1px;
  }
  .freeBtn {
    margin-top: 12px;
    text-align: right;
  }
  .name {
    font-weight: 600;
  }
  .el-icon-setting {
    transition: 1s;
    &:hover {
      transform: rotate(180deg);
      cursor: pointer;
    }
  }
  .fa {
    font-size: 24px;
    transition: all 0.3s;
    &:hover {
      cursor: pointer;
    }
  }
  a {
    line-height: 60px;
  }
  a.logout {
    color: #fff;
    text-decoration: none;
    &:hover {
      color: #20a0ff;
    }
  }
  i {
    font-size: 20px;
    line-height: 60px;
  }
  .logout {
    color: #fff;
    &:hover {
      color: #20a0ff;
    }
  }
}
.fa.nav-rotate {
  transform: rotate(90deg);
}
.row-right > div {
  text-align: center;
}
</style>
