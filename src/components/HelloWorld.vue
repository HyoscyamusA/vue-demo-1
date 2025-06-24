<template>
  <div class="hello">
    {{name}}
    {{ age > 60 ?'老年':'青年' }}
  </div>
  <input type="text" v-bind:value="name"/>
  <input type="text" :age="age"/>
  <img :src="src">
  <input type="button" value="保存" v-on
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      name:'张三',
      age:18
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
