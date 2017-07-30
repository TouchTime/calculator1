<template>
  <div id="app">
    <vheader></vheader>
    <input type="text" placeholder="生态系统">
    <router-link to="/goods">商品</router-link>
    <router-link to="/seller">卖家</router-link>
    <div>
      <input
      v-model="newTodoText"
      v-on:keyup.enter="addNewTodo"
      placeholder="Add a todo">
      <ul>
        <li
          is="todo-item"
          v-for="(todo, index) in todos"
          v-bind:key="index"
          v-bind:title="todo"
          v-on:remove="todos.splice(index, 1)">
        </li>
      </ul>
    </div>
    <router-view></router-view>
  </div>
</template>

<script  type="text/ecmascript-6">
  import vheader from './components/header/header'
  import vue from 'vue'
  vue.component('todo-item', {
    template: '<li>{{ title }}<button v-on:click="$emit(\'remove\')">X</button></li>',
    props: ['title']
  })
export default {
  name: 'app',
  components: {
   vheader
  },
  data () {
      return {
        newTodoText: '',
        todos: [
          'Do the dishes',
          'Take out the trash',
          'Mow the lawn'
        ]
      }
  },
  methods: {
      addNewTodo: function () {
          this.todos.push(this.newTodoText)
          this.newTodoText = ''
      }
  }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
