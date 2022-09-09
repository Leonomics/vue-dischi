<template>
  <div class="navContainer">
    <!--<h1>{{ msg }}</h1>-->
    <nav class="navbarStyle navbar navbar-light">
      <a class="navbar-brand" href="#">
        <img src="../assets/spotify.png" width="30" height="30" alt="">
      </a>
      <select @change="$emit('myGenreEmit', myGenre)" v-model="myGenre" class="selectpicker" aria-label="Default select example">
        <option v-for="(genre, i) in genres" :key="i" :value='genre'>{{genre}}</option>
      </select>
    </nav>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
  props: {
    genre:{
      type: String,
      
    }
  },
  data(){
    return{
      myGenre: "",
      genres: ["Rock", "Pop", "Jazz", "Metal"]
    };

  },
  
  methods:{
    prova(){
      console.log(this.myGenre)
    }
    /*select(){
      this.$emit
    }*/
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/general.scss';

  .navbarStyle{
    background-color: #2e3a46;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
  }
</style>
