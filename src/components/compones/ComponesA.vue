<template>
  <div>
      <div>
          <h3>A组件</h3>
         
          <p>{{isdata}}</p>
          <button v-on:click="click">A组件的按钮</button>
      </div>
  </div>
</template>

<script>
export default {
    data:()=>{
        return{
            
            isdata:true
        }
    },
    methods:{
        click:function(){
            // this.currentComponent=this.currentComponent===ComponesA ? ComponesB:ComponesA
            this.isdata= this.isdata===true? false:true;
        }
    }
}
</script>

<style>

</style>