<template>
    <div class="container">
        <h3 class="titoloW mt-4">Movies</h3>
        <div class="d-flex flex-wrap">
            <FilmCard v-for="(film, index) of paramFilms" :key="index" :singleFilm="film"/>
        </div>
        

        <h3 class="titoloW mt-5">Tv Series</h3>
        <div class="d-flex flex-wrap">
            <SerieTvCard v-for="(serie, index) of paramSerieTv" :key="index" :singleSerie="serie"/>
        </div>
    </div>
</template>




<script>
import FilmCard from '../components/FilmCard.vue'
import SerieTvCard from '../components/SerieTvCard.vue'

export default {
    name: 'MainComp',
    props:{
        paramFilms : Array,
        paramSerieTv : Array
    },
    components:{
        FilmCard,
        SerieTvCard
    }
}


</script>





<style lang="scss" scoped>

.titoloW {
    color: white;
}


/* .container{
    background-color: rgb(20, 20, 20);
} */


</style>