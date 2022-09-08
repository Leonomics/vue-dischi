<template>
    <div class="mainComponent">
      <div class="container mt-5">
            <div class="row gy-5 mx-auto">
        <div v-for="(disk,i) in listDisks" :key="i" class="col">
        <div class="card">
  <div class="card-body">
    <img class="card-img-top poster" :src="disk.poster" alt="Card image cap">
    <h5 class="card-title mt-3">{{disk.title}}</h5>
    <p style="color:grey">{{disk.author}}</p>
    <p style="color:grey">{{disk.year}}</p>
  </div>
</div>
    </div>
    </div>
        </div>
    </div>
      
    
    
</template>
  
<script>

import axios from "axios"; 

  export default {
    name: "MainComponent",
    
    data(){
    return  {
        listDisks: []
    };
    
  },
    created(){
    axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
                console.log(res.data)
                this.listDisks = res.data.response;
                
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

    .card{
      background-color: #2e3a46;
      width: 194px;
      height: 364px;
      text-align: center;
    }
    .poster{
      width: 160px;
      height: 160px;
    }
    .card-title{
      max-width: 160px;
      color: white;
    }
    .mainComponent{
      background-color: #1e2d3b;
    }
  </style>
  