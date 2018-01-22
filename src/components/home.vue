<template>
  <div>
    <div>  <a @click="submit">退出</a>  </div>
    <div style="padding: 50px;">{{user.name}}欢迎回家</div>
  </div>
</template>
<script>
  import { mapState } from 'vuex'
  import { mapActions } from 'vuex'
  import { USER_SIGNOUT } from '../store/user'
  export default {
    computed: mapState({ user: state => state.user }),
    methods: {
      ...mapActions([USER_SIGNOUT]),
      submit() {
        this.USER_SIGNOUT()
        this.$router.replace({ path: '/' })
      }
    }
  }
</script>
