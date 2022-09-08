<template>
  <div class="navContainer">
    <!--<h1>{{ msg }}</h1>-->
    <nav class="navbarStyle navbar navbar-light">
      <a class="navbar-brand" href="#">
        <img src="../assets/spotify.png" width="30" height="30" alt="">
      </a>
      <select v-model="genre" class="selectpicker" aria-label="Default select example">
        <option v-for="(genre, i) of genres" :key="i">{{genre}}</option>
      </select>
    </nav>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
  props: {
    msg: String,
    //genre: String,
  },
  data(){
    return{
      genre: "",
      genres: ["Rock", "Pop", "Jazz", "Metal"]
    };

  },
  computed: {
    filteredGenres() {
      return this.listDisks.filter((disk) => {
        const songGenre = disk.genre.toLowerCase()
        const genre = this.genre.toLowerCase()

        if (songGenre.includes(genre)){
          return true
        }
        else{
          return false
        }
      });
    }
  },
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
