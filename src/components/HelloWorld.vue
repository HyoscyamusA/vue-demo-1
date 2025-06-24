<template>
  <div class="hello">
    {{name}}
    {{ age > 60 ?'老年':'青年' }}
  
  <input type="text" v-bind:value="name"/>
  <input type="text" :age="age"/>
  <!---<img :src="src">-->
  <input type="button" value="保存" v-on:click="handleSave"/>
  <input type="button" value="保存" @click="handleSave"/>

  <input type="text" v-model="name" />
  <input type="button" value="修改" @click="handleChange"/>

  <div v-if="sex ==1">
    男
  </div>
  <div v-else-if="sex ==2">
    女
  </div>
  <div v-else>
    未知
  </div>
  
</div>
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
      age:18,
      sex:1
    }
  },
  methods:{
    handleSave(){
      alert('点击保存按钮')
    },
    handleChange(){
      this.name = '李四'
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
