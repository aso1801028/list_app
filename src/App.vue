<template>
  <div id="app">
    <hello-world v-bind:title="message"

    v-on:result-event="doAction"
    v-on:table="doAction"/>
    <p>{{ result }}</p>
    
    
    
  </div>
</template>

<script>
import HelloWorld from './components/Mylist.vue'


export default {
  name: 'App',
  components: {
    HelloWorld
    
  },
  
  methods:{
    doAction2:function(){
      //ここにデータを入れる
      
    },
    /*appAction:function(){
      this.result = '(*** you send:"'+ message +' ***)';
      
      //ここにデータを入れる
        var data = {
    items:[
      {name:'at'}
      ]
      }
    }*/
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
