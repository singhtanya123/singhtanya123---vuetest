<template>
<div class="main">
 <HelloWorld msg="Welcome to Your Vue.js App"/>
 <Dashboard/>

  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Dashboard from './components/Dashboard.vue';


export default {
  
  name: 'App',
  components: {
    HelloWorld,
    Dashboard
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 2%;
  margin-top: 60px;
}
.main{
  border: 5px white solid;
  width: 100%;
  height: 50%;
}
</style>
