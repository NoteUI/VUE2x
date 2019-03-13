# vuedev
# 最近面试经常有人针对没有使用过某些框架
# 本人觉得重点是开发者的工作经验与学习态度问题

1.安装vue-cli
   npm install -g vue-clie
2.初始化项目
  vue inti webpack my-project
3.进入项目
cd my-project
4.安装依赖
 npm install
5.启动项目
 npm run dev

#项目结构
index.html 项目根视图
static : 静态文件目录


子组件通过自定义事件传递给父组件数据
自定义事件中有两个参数 key是自定义事件名 参数2是你要传递的数据
子组件:@click="sendmsg"
          methods:{
             sendmsg(event){
                  this.$emit("send",this.msg)
}
}
父组件  @send="gotmsg"
          methods:{
              gotmsg(data){
                  console.log(data）
}
}

# 插槽的应用场景:数据相同但数据展示形式不同
单个插槽写法
  父组件:<son><p>我是插槽</p></son>
  子组件:<slot></slot>
具名插槽写法
  父组件:<son><p slot="s1">我是插槽</p></son>
  子组件:<slot name="s1"></slot>
作用域插槽:是由子组件传递数据给父组件
  父组件:<son><p slot-scope="prop">{{prop.text}}</p></son>
子组件:<slot text="我是数据传递"></slot>

# 过滤器
filters{
    moneyFormat(value){
        if(typeOf value === "number"){
           return "$"+value; 
       }else{
           return value;
       }
    }
}

# 路由
1.安装
npm install vue-router --save
2.
var router = new VueRouter(
routers:[{
    path:"/",
    component: page
}]
) //注意组件引入名已经改了