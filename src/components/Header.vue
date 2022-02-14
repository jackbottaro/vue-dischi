<template>
<div>
  <div id="top-bar">
  <img src="https://storage.googleapis.com/pr-newsroom-wp/1/2018/11/Spotify_Logo_CMYK_White.png" alt="Spotify_Logo_CMYK_White">
  </div>
</div>
</template>

<script>
export default {
  name: "Header",
  props: {

  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#top-bar{
height: 80px;
background-color: #2e3a46;
display: flex;
align-items: center;
}

img{
 width: 10%;
  height: auto;
  margin-left: 30px;

}
</style>
