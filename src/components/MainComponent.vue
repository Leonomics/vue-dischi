<template>
    <div>
        <div>
            <div>
        <div v-for="(disk,i) in listDisks" :key="i">
        <div class="card" style="width: 18rem;">
  <div class="card-body">
    <img class="card-img-top" :src="disk.poster" alt="Card image cap">
    <h5 class="card-title">{{disk.title}}</h5>
    <p>{{disk.author}}</p>
    <p>{{disk.year}}</p>
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
  </style>
  