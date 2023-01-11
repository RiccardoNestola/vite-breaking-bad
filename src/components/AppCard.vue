
<script>
import { store } from "../store"

export default {

    data() {
        return {
            store,
        }
    }

}



</script>

<template>
    <div class="col" v-for="element in store.CharactersList">
        <div class="card">
            <img :src="element.card_images[0].image_url" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title">{{ element.name }}</h5>
                <p class="card-text">{{ element.archetype }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss">

</style>