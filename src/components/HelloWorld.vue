<template>
  <div class="hello">
    <h1>你好</h1>
    <h2>{{msg}}</h2>
    <ul>
      <li v-for="(item, index) in list" :key="index">{{item}}</li>
    </ul>
    <main>
      <slot srgh='fffff' name='main' :list1="list1"></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      list:["标题1","标题2","标题3","标题4","标题5","标题6"],
      list1:["标题221","标题222","标题223","标题224","标题225","标题226"]
    }
  },
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
.red {
  height:25px;
  width:250px;
  background-color:red;
}
</style>
