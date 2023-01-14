
<script>
import { store } from "../store"
import axios from 'axios';
import AppSearch from "./AppSearch.vue"
import AppSelect from "./AppSelect.vue"



export default {

    components: {
        AppSearch,
        AppSelect
    },

    data() {
        return {
            store,
            ApiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0',

        }
    },

    methods: {

        searchForm(argA) {
            alert("ciao" + " " + argA)

        },

        /* mySelect(argA) {
            alert("ciao" + " " + argA)

        }, */

        mySelect(selectedArchetype) {
            axios.get(this.ApiUrl, {
                params: {
                    archetype: selectedArchetype


                }
            })
                .then((response) => {
                    console.log(response.data);
                    this.store.CharactersList = response.data.data;
                })
                .catch(function (error) {
                    console.log(error);
                });

        }


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


            <AppSelect @onSelect="mySelect" />

            <AppSearch @inputSearch="searchForm" />



            <div class="navbar-brand mb-0 d-flex flex-row-reverse pt-4">

                <p class="navbar-brand mb-0">Numero di card: {{ store.CharactersList.length }}</p>
            </div>

        </div>


    </header>
</template>

<style lang="scss" scoped>

</style>