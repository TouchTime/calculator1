<template>
  <div>
    <my-component></my-component>
    <my-component></my-component>
    <my-component></my-component>
    <my-components></my-components>
  </div>
</template>
<script type="text/ecmascript-6">
  import Vue from 'vue'
  // 注册

  Vue.component('my-component', {
      template: '<button v-on:click="counter += 1">{{ counter }}</button>',
      data: function () {
          return {
              counter: 0
          }
      }
  })
  var child = {
    template: '<div>A custom </div>'
  }
  export default {
      components: {
          'my-components': child
      },
      data () {
          return {

          }
      }
  }

</script>

<style lang="stylus" rel="stylesheet/stylus">
</style>
