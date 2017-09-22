<template>
  <div class="hello">
    <h1 v-text="hello"></h1>
    <p v-for="item in list" v-text="item.name+'__'+item.price"></p>
    <p v-text="msg"></p>
  </div>
</template>

<script>
export default {
  name: 'hello',
  mounted:function () {
    this.getDate();
  },
  data () {
    return {
      hello: 'Welcome to Your Vue.js App',
      msg:"",
      list:"",
    }
  },
  methods:{
      getDate(){
        this.list=[
          {
            name:"apple",
            price:35
          },
          {
            name:"orange",
            price:40
          },
          {
            name:"red",
            price:33
          }
        ]
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

a {
  color: #42b983;
}
</style>
