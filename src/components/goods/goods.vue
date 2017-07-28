<template v-if="loginType === 'username'">
  <div>
    <label>Username</label>
    <input placeholder="Enter your username" key="username-input">
    <button v-on:click="newclick">click me</button>
  </div>

</template>
<template v-else>
  <div>
    <label>Email</label>
    <input placeholder="Enter your email address" key="email-input">
    <button v-on:click="newclick">click me</button>
  </div>
</template>
<script type="text/ecmascript-6">
  export default {
      data () {
          return {
            newclick: function () {
                var loginType
                if (loginType === 'username') {
                  loginType = ''
                } else {
                  loginType = 'username'
                }
            }
          }
      }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
</style>
