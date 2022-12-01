<template>
    <div class="container">
        <h3 class="titoloW mt-4">Movies</h3>
        <FilmCard v-for="(film, index) of paramFilms" :key="index" :singleFilm="film"/>

        <h3 class="titoloW mt-5">Tv Series</h3>
    </div>
</template>




<script>
import FilmCard from '../components/FilmCard.vue'

export default {
    name: 'MainComp',
    props:{
        paramFilms : Array,
        paramSerieTv : Array
    },
    components:{
        FilmCard
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