<template>
  <HelloWorld msg="msg props 第二栏">
    <!-- v-slot="slotProps" 作用域插槽 -->
    <!-- <template v-slot:footer>  具名插槽-->
      <template #main="slotProps">
      <span>
        <h1>具名作用域插槽</h1>
      <ul>
        <li v-for="(item, index) in slotProps.list1" :key="index">{{item}}</li>
      </ul>
        <p class='red'>222222</p>
      </span>
    </template>
    <template #footer>
      <p>v-slot:footer 与 #main具名插槽</p>
      <a href="">111111111111</a>
      <p class='red'>333333</p>
    </template>
  </HelloWorld>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default { 
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.red {
  height:25px;
  width:250px;
  background-color:red;
}
</style>
