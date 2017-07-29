<template>
  <div>
    <div v-if="Math.random() > 0.5">我是seller</div>
    <div v-else>{{ author }}</div>

    <div v-if="type === 'A' ">A</div>
    <div v-else-if="type ===  'B' ">B</div>
    <div v-else-if="type === 'C' ">C</div>
    <div v-else>D</div>

    <button v-on:click.once="doThis()">增加</button>
    <p>{{ counter }}</p>
    <button v-on:click="counte += 1">增加1</button>
    <p>{{ counte }}</p>

    <input v-model="me" placeholder="edit me">
    <p>message is: {{ me }}</p>

    <input type="checkbox" id="checkbox" v-model="check_ed">
    <label for="checkbox">{{ check_ed }}</label>
  </div>

</template>
<script type="text/ecmascript-6">
  export default {
      data () {
          return {
              author: '在字符串模板中，如 Handlebars ，我们得像这样写一个条件块',
              type: 'A',
              counter: 0,
              counte: 1,
              me: 'hi',
              check_ed: false
          }
      },
    methods: {
      doThis: function () {
         this.counter += 1;
         console.log(this)
         return this.counter
      }
    }
  }
</script>

<style>
  button{
    width: 50px;
    height: 20px
  }
</style>
