<template>
<div>
<div class="container">
  <div class="card" v-for="album in library" :key="album.id">
    <img :src="album.poster" alt="">
    <p id="album-name">{{ album.title }}</p>
    <p id="author-name">{{ album.author }}</p>
    <span id="relase-year">{{ album.year }}</span>
  </div>
</div>  
  
</div>
</template>

<script>
import axios from "axios";
export default {
  name: "Main",
  props: {

  },
  data() {
    return {
      library: [],
    }; 
  },
  mounted() {
    axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {
      this.library = res.data.response;
    })
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
  margin: 0 auto;
  width: 1200px;
  margin-top: 80px;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

}
.card{
  background-color: #b0b0b029;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 200px;
  padding: 30px;
  border-radius: 15px;
  margin: 20px;
}

img{
   width: 150px;
  height: auto;
  margin-bottom: 15px;
}

#album-name{
  color: white;
  text-transform: uppercase;
  margin-bottom: 10px;
  text-align: center;
  font-weight: bold;

}

#author-name{
  color: lightgray;
  margin-bottom: 5px;
  text-align: center;



}

#relase-year{
  color: lightgray;

}
</style>
