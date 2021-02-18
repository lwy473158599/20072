<template>
  <div id="app">
  <keep-alive include="ComponesA">
    <component :is="currentComponent"></component>
  </keep-alive>
  
    <button v-on:click="click">点我切换组件</button>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Son from "./components/Son";
import Fang from './components/componse/parent';
import Cha from './components/componse/Chacha';
import ComponesA from './components/compones/ComponesA'
import ComponesB from './components/compones/ComponesB'
export default {
  name: "App",
  components: {
    HelloWorld,
    Son,
    Fang,
    Cha,
    ComponesA,
    ComponesB
  },
  data(){
    return{
    currentComponent:ComponesA

    }
  },
  methods:{
    click:function () {
      this.currentComponent=this.currentComponent===ComponesA ? ComponesB:ComponesA
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
