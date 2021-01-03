<template>
  <div id="app">
<!--    <div id="nav">-->
      <Navbar></Navbar>
<!--      <router-link to="/">Home</router-link> |-->
<!--      <router-link to="/about">About</router-link>-->
<!--    </div>-->
    <router-view/>
    <TheFooter></TheFooter>

  </div>
</template>

<script>
import Navbar from "@/components/UI/Navbar";
import TheFooter from "@/components/UI/TheFooter";
export default{
  components:{
    Navbar,
    TheFooter
  }
}
</script>
<style>
:root {
  --clr-orange-1: hsl(12, 83%, 98%);
  --clr-orange-2: hsl(14, 91%, 95%);
  --clr-orange-3: hsl(12, 89%, 89%);
  --clr-orange-4: hsl(13, 87%, 82%);
  --clr-orange-5: hsl(13, 88%, 68%);
  --clr-orange-6: hsl(13, 88%, 55%);
  --clr-orange-7: hsl(13, 74%, 49%);
  --clr-orange-8: hsl(13, 74%, 33%);
  --clr-orange-9: hsl(13, 73%, 25%);
  --clr-orange-10: hsl(13, 73%, 16%);
  /* primary/main color */
  /*--clr-primary-5: #49a6e9; */
  --clr-mc: #2196f3;
  --clr-bluePrimary: #007bff;
  --clr-blueHover: #0069d9;
  --weird-blue:  #42b983;


  --clr-primary-1: hsl(205, 86%, 17%);
  --clr-primary-2: hsl(205, 77%, 27%);
  --clr-primary-3: hsl(205, 72%, 37%);
  --clr-primary-4: hsl(205, 63%, 48%);
  /* primary/main color */
  --clr-primary-5: hsl(205, 78%, 60%);
  /* lighter shades of primary color */
  --clr-primary-6: hsl(205, 89%, 70%);
  --clr-primary-7: hsl(205, 90%, 76%);
  --clr-primary-8: hsl(205, 86%, 81%);
  --clr-primary-9: hsl(205, 90%, 88%);
  --clr-primary-10: hsl(205, 100%, 96%);
  /* darkest grey - used for headings */
  --clr-grey-1: hsl(209, 61%, 16%);
  --clr-grey-2: hsl(211, 39%, 23%);
  --clr-grey-3: hsl(209, 34%, 30%);
  --clr-grey-4: hsl(209, 28%, 39%);
  /* grey used for paragraphs */
  --clr-grey-5: hsl(210, 22%, 49%);
  --clr-grey-6: hsl(209, 23%, 60%);
  --clr-grey-7: hsl(211, 27%, 70%);
  --clr-grey-8: hsl(210, 31%, 80%);
  --clr-grey-9: hsl(212, 33%, 89%);
  --clr-grey-10: hsl(210, 36%, 96%);
  --clr-white: #fff;
  --clr-red-dark: hsl(360, 67%, 44%);
  --clr-red-light: hsl(360, 71%, 66%);
  --clr-green-dark: hsl(125, 67%, 44%);
  --clr-green-light: hsl(125, 71%, 66%);
  --clr-black: #222;
  --transition: all 0.3s linear;
  --spacing: 0.1rem;
  --radius: 0.25rem;
  --light-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
  --dark-shadow: 0 5px 15px rgba(0, 0, 0, 0.4);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  /*padding: 30px;*/

}

/*#nav a {*/
/*  font-weight: bold;*/
/*  color: red;*/
/*}*/

/*#nav a.router-link-exact-active {*/
/*  color: #42b983;*/
/*}*/




</style>
