<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    
  <input type ="text" v-model="input">
  <button v-on:click="doAction">click</button>
  <hr>
  <p v-html="list"></p>
  <p><table><tr><th>mylist</th></tr>
     <tr><td>{{ list }}</td></tr>
    </table></p>

  <p>{{ list }}</p>
  <copted v-model="msg"></copted>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    title: String,
    //message: String,
    list:String,
    
  },
  data:function(){
    return {
      message:'what your name?',
      input:'mylist',
    };
  },
  //ここにmylistで入れ
  methods:{
    doAction:function(){
      /*var list{
        
      }*/
      //this.list = this.input + 'さん';
      this.list = this.input + document.createElement('table');
      var row = table.insertRow( -1 );
      //ここを書き換える？
      this.$emit('table',this.input);
      this.$emit('result-event',this.input);
    }
   
  }
}
</script>

<style>
div{
  margin:0px;
  padding: 0px;
  text-align: center;
}
h1{
  font-size: 20pt;
  font-weight: bold;
  text-align: center;
  color: black;
  margin: 0px;
}

table tr th{
  padding: 0px;
  text-align: center;
  color:white;
  background-color: black;
  margin: 0px;
}
table tr td{
  padding: 0px;
  text-align: center;
  border:1px solid gray;
  margin: 0px;
}

</style>
