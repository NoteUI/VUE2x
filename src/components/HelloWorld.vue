<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>模板语法</h2>
    <ul class="tipBox">
      <span>{{乐乐}}</span>
      <span>{{1+1}}</span>
      <span>{{"lele"}}</span>
      <span>{{zimu.split('').reverse().join('')}}</span>
      <span>{{0>10 ? '判断对的' : '错的0不大于10'}}</span>
      <li>
        <a target="_blank"> {{url}} </a>
      </li>
    </ul>
    <h2>基本指令</h2>
    <ul>
      <li class="tipBox">
        <span v-text="msg"></span>
        <span v-html="href"></span>
        <span v-bind:class="btns">按钮</span>
        <span v-bind:title="tips">title标题</span>
      </li>
      <li> <a href="http://router.vuejs.org/"target="_blank"> vue-router </a> </li>
      <li> <span v-html="href"></span> </li>
    </ul>
    <h2>条件渲染</h2>
    <ul>
      <li class="tipBox">
        <template v-if="show">
          <span>条件显示</span>

        </template>
        <template v-else-if="sho">
          <span>v-else-if显示</span>
        </template>
        <template v-else>
          <span>条件不显示</span><span>条件测试</span>
        </template>
      </li>
    </ul>
    <ul class="listBox">
      <li v-for="item in names">{{item}}</li>
      <li v-for="(items,index) in names" :key="index">{{ items }}-{{ index }}</li>
      <li v-for="lele in user">
       <span>{{lele.name}}</span>
       <span>{{lele.age}}</span>
      </li>
    </ul>
    <ul>
      <button v-on:click="num+=1" >dianji</button>
      <p>{{num}}</p>
      <button class="btn btn-primary" v-on:click="handerClick" >取反显示隐藏</button>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      num:1,
      msg: '欢迎进入我的项目',
      乐乐:"乐乐的页面",
      zimu:'welcome',
      url:'http://www.baidu.com',
      href:'<a href="http://www.harryword.com" target="_blank">harryword</a>',
      btn:'btn',
      tips:'title标题动态改变',
      show:false,
      sho:true,
      names:["harry","lee","ele"],
      user:[
        {
          id:1,
          name:"harry",
          age:15,
        }, 
        {
          id:2,
          name:"gsdfgsd",
          age:15,
        }, 
        {
          id:3,
          name:"hadfgdsfgdfgrry",
          age:15,
        }, 
        {
          id:4,
          name:"hadfsdfasdfasdfsarry",
          age:15,
        }
       ]
    }
  },
  methods:{
  handerClick(){
      console.log(this);
      this.show = !this.show;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1, h2 {
  font-weight: normal;
}
h2{margin: 1em auto; font-weight: bold; font-size: 2em; color: green;}
ul {
  list-style-type: none;
  padding: 0;
}
.tipBox span{    background: #5bc0de;
  margin-bottom: 10px;
    padding: 5px 20px;
    color: #fff;
    text-shadow: 1px 1px 1px rgba(0,0,0,.1);
    -webkit-transition: background-color .35s ease-in-out;
    -moz-transition: background-color .35s ease-in-out;
    -ms-transition: background-color .35s ease-in-out;
    -o-transition: background-color .35s ease-in-out;
    transition: background-color .35s ease-in-out;
}

li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.btns{background: #ff0 !important; color: #000 !important;}
</style>
