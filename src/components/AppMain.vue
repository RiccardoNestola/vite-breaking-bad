<script lang="js">

import { store } from "../store"
import axios from 'axios';
import AppCard from './AppCard.vue'

export default {

    components: {
        AppCard,
    },

    data() {
        return {
            store,
            ApiUrl: 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0',
        }
    },
    methods: {
        getCharacters(selectedArchetype) {
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
    },

    created() {
        this.getCharacters();
    }

}
</script>

<template>
    <main>
        <div class="container mt-4">
            <div class="row row-cols-1 row-cols-md-3 row-cols-lg-5 g-4">
                <AppCard />
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    padding-bottom: 2rem;
}
</style>