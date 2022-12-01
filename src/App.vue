<template>
  <div id="app">
    
    <NavbarSection @emitSearch="searchFilms" />
    <MainComp :paramFilms="arrayFilms"/>
    <SerieTvCard/>

    <!-- <FilmCard/> -->



  </div>
</template>

<script>
import NavbarSection from './components/NavbarSection.vue'
/* import FilmCard from './components/FilmCard.vue' */
import MainComp from './components/MainComp.vue'
import SerieTvCard from './components/SerieTvCard.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    NavbarSection,
    MainComp,
    SerieTvCard
    /* FilmCard */
  },
  data() {
    return{
      arrayFilms: [],
      serieTv: []
    }
  },
  methods: {
    searchFilms(valoreEmit){
      axios.get( 'https://api.themoviedb.org/3/search/movie?api_key=67a7569e9af4ccdbb00447d7c0733e96&query=' + valoreEmit )
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
    height: 100%;
    padding-bottom: 5%;
}


</style>
