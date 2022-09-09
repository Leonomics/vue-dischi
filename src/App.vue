<template>
  <div id="app">
    <HeaderComponent @myGenreEmit="selectDisk"/>
    <MainComponent :myReceivedGenre="mySelectedGenre"></MainComponent>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";


export default {
  name: "App",
  data(){
    return  {
      mySelectedGenre:'',
    };
    
  },
  
  components: {
    HeaderComponent,
    MainComponent
},
methods: {
  selectDisk(myGenre){
    console.log(myGenre)
    this.mySelectedGenre = myGenre
  }
}
};
</script>

<style lang="scss">
  @import './styles/general';
</style>
