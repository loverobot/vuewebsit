<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>可以试试</h2>
    <a href="#/detail">
       <img src="../assets/logo.png">
    </a>
  </div>
</template>

<script>
/**$(function(){
  $('body').append('<div>这里是jquery控制的区域</div>');
});**/
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '好东西'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  text-align:center;
}
h1, h2 {
  font-weight: normal;
  text-align:center;
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
