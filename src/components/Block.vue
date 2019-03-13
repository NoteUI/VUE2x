<template>
  <div class="block">
    <ul>
      <li v-on:click.once="getinfo(index,$event)" v-for="(name,index) in names">{{name}}</li>
      <!-- <li v-on:click="getInfo">{{name}}</li> -->
    </ul>
    <ul>
      <input type="text" v-on:keyup.enter="getKeyinfo" class="input">
      <button v-on:click="getpush">按钮</button>  
      <button v-on:click="getodd">奇数</button>  
    </ul>
  </div>
</template>

<script>
export default{
  data(){
    return{
      names:["harry","dede","lili","lele"],
      numbers:[1,2,3,4,5,6,7,9,8]
    }
  },
  methods:{
    getinfo(data,event){
      console.log(this.names[data])
      console.log(data)
      console.log(event)
    },
    getKeyinfo(){
        console.log(event) 
    },
    getpush(){
      this.names.push("添加的");
    },
    getodd(){
      this.numbers.filter(function (num) {
        if (num % 2 !== 0) {
          console.log(num)
        }
        return num % 2 !== 0;
      })
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li { width: 80%;  margin: 10px auto; border-bottom: 1px solid rgba(0,0,0,0.2);
  font-size: 2em; color: green;
}
a {
  color: #42b983;
}
.btn{background: #ff0 !important; color: #000 !important;}
</style>
