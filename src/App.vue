<template>
  <div id="app">
    <HeaderComponent/>
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
methods: {
  selectDisk(myGenre){
    console.log(myGenre)
  }
}
};
</script>

<style lang="scss">
  @import './styles/general';
</style>
