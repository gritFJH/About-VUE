<template>
  <div class="hello">
   {{"变量："}} {{ hello }}
    <br>
  {{"直接运算："}} {{1+1}}
  <br>
 {{"字符串："}} {{'haha'}}
  <br>
  {{"三元运算符："}}{{0>10?'对的':'错的'}}  <div>中只能存在单行语句！</div>
  <p>{{flag}}</p>
  <p v-html="hello"></p>
  <p v-text="hello"></p>

  <span v-bind:class="haha">哈哈哈，我绑定了haha，我是红色</span>
  <span v-bind:title="ts">提示</span>

  <div>
    <p v-if="show">我是if为true看到的</p>
    <p v-else>我是if为false看到的</p>
  </div>
  <div class="list">
    <ul>
      <li v-for="(name,index) in names" v-bind:key="index">{{ name }}-{{ index }}</li>
    </ul>
    <ul>
      <li v-for="(item,index) in user" :key="index">
        <span>{{ item.name }}</span>
        <span>{{ item.age }}</span>
      </li>
    </ul>
  </div>
  <button v-on:click="num+=1;">按钮</button>
  <div><p>{{num}}</p></div>
  <button v-on:click="handlerClick">事件按钮</button>



  </div>
</template>


<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      num:1,
      hello:"<p>Hello,VUE</p>",
      flag:"我是flag",
      haha:"haha",
      ts:"我是提示",
      show:true,
      names:["luocheng","iwen","david"],
      user:[
        {
          id:0,
          name:"iwen",
          age:20
        },
        {
          id:1,
          name:"ime",
          age:200
        },
        {
          id:2,
          name:"ice",
          age:29
        }
      ]
    }
  },
  methods:{
    handlerClick(){
      //alert(this);
      //console.log(this);
      //this指向当前组件，当前组件的所有属性都被绑定到了组件对象中，包括自定义的属性和方法
      // alert("我是事件");
      //this 来索引当期的data中的数据
      this.show=!this.show;
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
.haha{
  color: red;
}
</style>
