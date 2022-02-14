<template>
 <div>
   <Header />
   
   <Main />
 </div>
</template>

<script>
import Main from "./components/Main.vue";
import Header from "./components/Header.vue";


export default {
  name: "App",
  components: {
    Main,
    Header,
  },
};
</script>

<style lang="scss">

*{
margin: 0;
padding: 0;
box-sizing: border-box;
font-family: sans-serif;

}
body {
background-color: #1e2d3b;

}



body { background: #003149; }

h1, h2, h3, p {
  margin: 0 0 .5em;
}

h1 {
  font-weight: 800; // @font-weight-bold
  font-size: 118px;
  line-height: 1;
}

h2 {
  font-weight: 700; // @font-weight-bold
  font-size: 60px;
  line-height: 1.2;
}

h3 {
  font-weight: 700; // @font-weight-bold
  font-size: 40px;
  line-height: 1.2;
}

p.lead {
  font-weight: 400; // @font-weight-book
  font-size: 20px;
  line-height: 1.5;
}

p {
  font-weight: 400; // @font-weight-book
  font-size: 18px;
  line-height: 1.5;
}
</style>
