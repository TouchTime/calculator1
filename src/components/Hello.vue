<template>
  <div class="hello">{{ fullName }}
    <a :class="{ miss_a: missB, missActive: istrue }">{{ msg }}</a>
    <div :class="active">{{mi}}</div>
  </div>

</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'word',
      missB: true,
      istrue: false,
      active: {
          miss_a: true,
          wrap: true
      },
      firstName: 'Foo',
      lastName: 'Bar',
      fullName: 'Foo Bar'
    }
  },
  computed: {
      mi: function () {
          return this.msg.split('').reverse().join('');
      }
  },
  watch: {
    firstName: function (val) {
      this.fullName = val + ' ' + this.lastName
    },
    lastName: function (val) {
      this.fullName = this.firstName + ' ' + val
    }
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

.wrap{
  background:#000;
  width:40px;
  height:20px;
}
.miss_a{
  color:red
}

</style>
