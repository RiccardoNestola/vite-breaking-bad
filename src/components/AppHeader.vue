
<script>
import { store } from "../store"




export default {

    components: {

    },

    data() {
        return {
            store,

        }
    },

    methods: {


    }
}


</script>

<template>
    <header>
        <nav class="navbar navbar-dark bg-dark">
            <div class="container-fluid">
                <span class="navbar-brand mb-0 h1">YU GI OH</span>
            </div>
        </nav>

        <div class="container">




            <!--  <AppSearch @inputSearch="searchForm" /> -->


            <div class="navbar-brand mb-0 d-flex flex-row-reverse pt-4">

                <p class="navbar-brand mb-0">Numero di card: {{ store.CharactersList.length }}</p>
            </div>



        </div>


    </header>
</template>

<style lang="scss" scoped>

</style>