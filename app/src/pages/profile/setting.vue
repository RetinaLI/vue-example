<template>
<div>
    <el-input v-model="userName" placeholder="用户名："></el-input>
</div>
</template>

<script>
// import { ProfileService } from '@/services/profile';
import { STORE_MUTATION_MAP } from '@/stores';
import { mapState } from 'vuex';
// let profileService = new ProfileService();

export default {
  name: 'profile-setting',
  metaInfo: {
    title: 'profile-setting'
  },
  computed: {
    ...mapState(['currentUser']),
    userName: {
      get () {
        return this.currentUser && this.currentUser.name;
      },
      set (value) {
        this.$store.commit(STORE_MUTATION_MAP.UPDATE_CURRENT_USER, { name: value });
      }
    }
  },
  components: {
  }
};
</script>

<style>
</style>
