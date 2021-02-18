<template>
  <div>
      <p>我是儿子</p>
      <button v-on:click="click">开始传送</button>
      <input type="text" v-model="msg">
      <input type="text" v-model="mug">
     
  </div>
</template>

<script>
export default {
    data(){
        return{
            mag:'我是child儿子传递的数据',
            msg:'',
            mug:''
        }
    },
    methods:{
        click:function(){
            //自定义事件
            this.$emit('onEvent',this.mag)
            this.$emit('onInput',this.msg)
        }
    },
    watch:{
        mug(newVal){
          
            this.$emit('onInval',newVal)
        }
    }
}
</script>

<style>

</style>