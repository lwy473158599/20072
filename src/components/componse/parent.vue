<template>
  <div>
      <p>我是你爹</p>
      <Child v-on:onEvent="getMsg" v-on:onInput='getInput' v-on:onInval='getVal'/>
      <p>{{data}}</p>
      <p>{{val}}</p> <span>我是input v-defalt传递过来的数据</span>
      <p>{{vst}} 实时获取的数据</p>
  </div>
</template>

<script>
import Child from './Child'
export default {
  
    data(){
        return{
            data:'',
            val:'',
            vst:''
        }
    },
    components:{
        Child
    },
    methods:{
        getMsg:function(data){
            this.data=data
            //console.log(data)
        },
       getInput:function(val){
           //console.log(val)
           this.val = val
       } ,
       getVal:function(val){
           console.log(val)
           this.vst = val
       }
    }
    
}
</script>

<style>

</style>