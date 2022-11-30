<template>
    <div>
        <FilmCard :filmsData="paramFilms"/>
    </div>
</template>




<script>
import FilmCard from '../components/FilmCard.vue'

export default {
    name: 'MainComp',
    props:{
        paramFilms : Array
    },
    components:{
        FilmCard
    }
}


</script>





<style lang="scss" scoped>

</style>