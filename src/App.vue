<template>
  <div id="app">
    <HeaderComponent msg="Welcome to Your Vue.js App" />
    <MainComponent></MainComponent>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";


export default {
  name: "App",
  data(){
    return  {
      
    };
    
  },
  components: {
    HeaderComponent,
    MainComponent
},
};
</script>

<style lang="scss">
  @import './styles/general';
</style>
