<template>
  <p>
  <label>    
    <input type="checkbox" v-model="isShow"> isShow: {{ isShow }}
  </label>
  </p>
  <img v-if="isShow"  alt="Vue logo" src="./assets/logo.png">

  <HelloWorld msg="Welcome to Your Vue.js App" appvueused="傳入的字串" />
  <p> {{customid}} </p>
  <p> {{customna}} </p>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  props:{
  },
  data () {
    return {
    isShow:false ,
    customid :'App.vue 本身的 data',
    customna :'App.vue 本身的 data 第二項'
    }
   // created() {
   //   console.log('created');
   // }
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
</style>
