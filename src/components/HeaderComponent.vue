<template>
  <div class="hello">
    <!--<h1>{{ msg }}</h1>-->
    <nav class="navbarStyle navbar navbar-light">
      <a class="navbar-brand" href="#">
        <img src="../assets/spotify.png" width="30" height="30" alt="">
    </a>
</nav>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/general.scss';

  .navbarStyle{
    background-color: #2e3a46;
  }
</style>
