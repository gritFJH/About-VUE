<template>
  <!-- 在template中，只能存在一个根组件，div有且只有一个 -->

  <div class="event">
      <ul>
        <li v-on:click="getItenInfo(index,$event)" v-for="(name,index) in names" :key="index">{{name}}</li>
      </ul>
  </div>

</template>



<script>
// 要导出可被外部访问
export default {
  data(){
    return{
      names:["iwen","ime","ice"]
    }
  },
  methods:{
    getItenInfo(data,event){
      //事件中的默认参数是event
      console.log(this.names[data]);
      console.log(data);
      console.log(event);//打印的是当前的event对象
    }
  }
}
</script>


<style>

</style>
