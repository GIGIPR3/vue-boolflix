<template>
    <div class="container m-auto mt-5 titoloW">

        <div class="d-flex">

            <div class="card m-2" id="carta">

                ciao

            </div>

            <!-- <div class="card m-2">

                

            </div>
            <div class="card m-2">

                

            </div>
            <div class="card m-2">

                

            </div>
            <div class="card m-2">
                
                
                
            </div>
            <div class="card m-2">
                
                

            </div> -->


        </div>


    </div>

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
    width: 200px;
    background-color: rgb(37, 37, 37);
}

.titoloW {
    color: white;
}
</style>