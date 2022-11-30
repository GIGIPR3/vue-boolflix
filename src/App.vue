<template>
  <div id="app">
    
    <NavbarSection/>

    <FilmCard/>



  </div>
</template>

<script>
import NavbarSection from './components/NavbarSection.vue'
import FilmCard from './components/FilmCard.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    NavbarSection,
    FilmCard
  },
  data() {
    return{
      arrayFilms: []
    }
  },
  methods: {
    searchFilms(valoreEmit){
      axios.get( 'https://api.themoviedb.org/3/search/movie?api_key=e99307154c6dfb0b4750f6603256716d&query=' + valoreEmit )
      .then((res)=>{
        this.arrayFilms = res.data.results
      })
    }
  }
}



</script>

<style lang="scss">
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */

#app{
    background-color: rgb(20, 20, 20);
    height: 100vh;
}


</style>
