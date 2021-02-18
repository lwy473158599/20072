<template>
  <div>
      <slot name="header" v-bind:msg="message"></slot>
      <div>插槽内容</div>
      <slot name='float'></slot>
  </div>
</template>

<script>
export default {
    data(){
        return{
            message:'我是儿子传递过来的数据'
        }
    }
}
</script>

<style>

</style>