<template>
  <div>
    <div v-if="Math.random() > 0.5">我是seller</div>
    <div v-else>{{ author }}</div>

    <div v-if="type === 'A' ">A</div>
    <div v-else-if="type ===  'B' ">B</div>
    <div v-else-if="type === 'C' ">C</div>
    <div v-else>D</div>
  </div>

</template>
<script type="text/ecmascript-6">
  export default {
      data () {
          return {
              author: '在字符串模板中，如 Handlebars ，我们得像这样写一个条件块',
              type: 'A'
          }
      }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
</style>
