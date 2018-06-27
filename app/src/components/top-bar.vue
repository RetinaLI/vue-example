<!-- 顶部导航组件 -->
<!-- 使用说明：<top-bar></top-bar> -->
<template>
    <div id="topbar-wrap">
        <el-row type="flex" justify="space-between">
            <el-col :span="12">
                <a href="/">首页</a>
                <a href="/products">产品</a>
                <a href="/profile">控制台</a>
                <a href="/docs/api/detail">接口详情</a>
            </el-col>
            <el-col :span="12">
                <el-row type="flex" class="row-right" justify="end">
                    <el-col :span="12">
                        <a class="animated fadeIn">Hi，{{currentUser && currentUser.name}}</a>
                    </el-col>
                    <el-col :span="12">
                        <i class="fa fa-sign-out logout" title="退出" @click.prevent="logout"></i>
                    </el-col>
                </el-row>
            </el-col>
        </el-row>
    </div>
</template>
<script>
import { mapState } from 'vuex';
export default {
  name: 'top-bar',
  data () {
    return {};
  },
  computed: {
    ...mapState(['currentUser'])
  },
  methods: {
    logout () {
    }
  },
  watch: {

  }
};
</script>
<style scoped lang="scss">
#topbar-wrap {
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
