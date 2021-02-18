<template>
  <div>
    <div>
      <p>{{ num }}</p>
      <button v-on:click="click">随机数</button>
    </div>
    <div>
      <p :class="{'box':isbox}" v-on:click='colo'>点我会变颜色</p>
      <p :style="{color:'pink',fontSize:'20px'}">行内样式</p>
    </div>
    <div>
      输入框
      <input type="text" v-model="msg">
      <p>{{msg}}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      isbox:false,
      msg:''
    };
  },
  methods: { //点击对象专用
    click: function () { //数据加加
      var ss = ~~(Math.random() * (30 - 1));
      if (this.num >= 100) {
        this.num = 100;
        return;
      } else {
        this.num = this.num + ss;
      }
    }, 
    colo:function(){
      this.isbox = !this.isbox
    }
  },
 watch:{
   num:function(newVal,oldVal){
      console.log(newVal,oldVal)

   }
 } 
};
</script>

<style>
.box{
  color: red;
}
</style>