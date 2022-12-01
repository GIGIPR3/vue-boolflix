<template>

            <div class="card m-2 " id="carta">

                <div class="w-100 h100 ">
                    <img src="{singleFilm.poster_path}" alt="">
                </div>

            </div>

        <!-- <h5 class="titoloW"> {{ title }} </h5> -->


</template>


<!-- v-for="(elem, index) in paramFilm" :key="index" :singleFilm="elem" -->


<script>


export default {
    name: 'FilmCard',
    props: {
        singleFilm: Object
    }
}

/* for( let i = 0; i < 6; i++ ){
    
} */


</script>


<style lang="scss" scoped>
.card {
    height: 300px;
    width: 184px;
    background-color: rgb(37, 37, 37);
    border-radius: 0px;
}

.titoloW {
    color: white;
}
</style>