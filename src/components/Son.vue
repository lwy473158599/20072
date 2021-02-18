<template>
<div>
    <div>
        <p>{{num}}</p>
    <button v-on:click="click">我是独立的组件</button>
    </div>
    <div>
        <p>我下头是传递过来的数据</p>
        <p>{{title}}:{{num}} {{arr}}</p>
    </div>
</div>
</template>

<script>
export default {
    data(){
        return{
            num:0,
        }
    },
    methods:{
        click:function(){
            this.num++
        }
    },
    props:{
        title:{ //这个名字必须和传递过来的名字一致
        type:[Number,String],
        default:'默认值'
        },
        arr:{
            default:function () {
                return['默认值']
            }
        }
    }
}
</script>
    
<style scoped> 
    

</style>