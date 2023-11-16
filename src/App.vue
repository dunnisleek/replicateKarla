<template>
  <!-- <navBar/> -->
  <home-page></home-page>
</template>

<script>
import homePage from './components/homePage.vue'
// import navBar from './components/navBar.vue'


export default {
  name: 'App',
  components: {
   homePage,
  //  navBar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@400;600&display=swap');
#app {
  font-family: 'Titillium Web', sans-serif;
 
}


</style>
