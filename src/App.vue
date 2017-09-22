<template>
  <div id="app">
    <img src="./assets/logo.png">
    <myHeader></myHeader>
    <div class="content">
      <div class="left">

      </div>
      <div class="right">
        <router-view></router-view>
      </div>

    </div>
    <myFooter></myFooter>

  </div>
</template>

<script>
  import  myHeader from "./components/header.vue";
  import  myFooter from  "./components/footer.vue";
export default {
  name: 'app',
  components:{
    myHeader:myHeader,
    myFooter:myFooter
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
.content{
  width: 100%;
  height: 600px;
}
  .left{
    float: left;
    width: 30%;
    height: 100%;
    outline: 1px solid black;
  }
  .right{
    float: right;
    width: 70%;
    height: 100%;
    outline: 1px solid red;
  }
</style>
