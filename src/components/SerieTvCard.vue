<template>



            <div class="card m-2" >

                <!-- <h5 class="titoloW"> {{ title }} </h5> -->

            </div> 



</template>





<script>


export default {
    name: 'SerieTvCard',
    props:{
        singleSerie: Object
    }
}




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