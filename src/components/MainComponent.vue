<template>
    <div class="hello">
        <div class="container">
    <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col">
      2 of 3
    </div>
    <div class="col">
      2 of 3
    </div>
  </div>
  <div class="row">
    <div class="col">
      1 of 3
    </div>
    <div class="col">
      2 of 3
    </div>
    <div class="col">
      3 of 3
    </div>
  </div>
</div>
    </div>
  </template>
  
<script>

import axios from "axios"; 

  export default {
    name: "HeaderComponent",
    props: {
      msg: String,
    },
    data(){
    return  {
        listDiscs: []
    };
    
  },
    created(){
    axios
                    .get('https://flynn.boolean.careers/exercises/api/array/music')
                    .then((res) => {
                console.log(res.data.response)
                this.listDiscs = res.data;
            });
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
  