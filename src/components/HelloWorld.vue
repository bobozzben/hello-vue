<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ appvueused }} property給外面傳入，這裏顯示</h1> <!-- 這裏要接且顯示 -->
    <p>
      HelloWorld.vue 的內容 For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h1> {{ customid }}</h1>
      <ul>
        <li v-for="item in arr" :key="item.id"  >{{ item }}</li>
      </ul>
      <ul>
        <li v-for="(item,index) in arr" :key="item.id"> {{index}} /{{item}} </li>
      </ul>
      <ul>
        <li v-for="val in book" :key="val.id" >{{val}} </li>
      </ul>
      <ul>
        <li v-for="(val,key) in book" :key="val.id"  > {{key}} /{{val}} </li>
      </ul>
  </div>
</template>

<script>
export default {
  props: {  // property section
    msg: String,
    appvueused:String,
  },
  data () {  //data section
    return {
    customid :'HelloWorld 裏的 data' ,  //variable
    arr: ['008', 'JS', 'is', 'awesome'], //array 
    book: {  // object
      title: '08js',
      author: 'Kuro',
      publishedAt: '2021/11',
     }
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
