<template>

    <div class="navbar">
        <div class="container m-auto">
            <div>
                <img src="../assets/pngegg (1).png" alt="" class="logo">
            </div>
            <div>

                <input type="text   " name="" id="search" v-model="searchImput"
                    placeholder="Cerca qui il Film o Serie Tv..." @keyup="$emit('emitSearch', searchImput)">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
        </div>

    </div>

</template>

<script>
export default {
    name: 'NavbarSection',
    data() {
        return {
            searchImput: ''
        }
    }
}
</script>


<style lang="scss" scoped>
.navbar {
    background-color: rgb(20, 20, 20);
    /* background-color: rgb(37, 37, 37); */
    height: 70px;

}

.logo {
    width: 140px;
    margin-left: 20px;
}

.fa-solid {
    color: white;
    margin-left: 15px;
}


#search {
    border: 0px;
    background-color: rgb(20, 20, 20);
    color: white;
    width: 210px;
    font-style: italic;
    border-bottom: 1px solid white;
}
</style>