
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
                <h4 class="card-title">{{ element.name }}</h4>
                <p class="card-text">{{ element.archetype }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card-body {

    height: 80px;
}

h4 {
    font-size: .8rem;
}

p {
    font-size: .6rem;
}
</style>