<template>
  <div id="app">
    <temp message="an222dy1"></temp>
    <home></home>
    <mycomp></mycomp>
    <three></three>
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <cpt1></cpt1>
    <cpt3 :level="1">hello friend</cpt3>
    <cpt2 :items="items"></cpt2>
  </div>
</template>

<script>
import temp from './components/temp.vue'
import home from './components/home.vue'
import mycomp from './components/mycomp.vue'
import three from './components/three.vue'
import cpt3 from './components/cpt3.vue'
import cpt2 from './components/cpt2.vue'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      message:'hello',
      items:[  
          {  
              name:'a',  
              id:0  
          },  
          {  
              name:'b',  
              id:1  
          },  
          {  
              name:'c',  
              id:2  
          }  
      ],
      lists:[]
    }
  },
  components:{
    temp,
    home,
    mycomp,
    three,
    cpt3,
    cpt2,
    cpt1:{
      render: function (h) {
        return (<h1>hahahahaha</h1>);
      }
    }
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

h1, h2 {
  font-weight: normal;
}
</style>
