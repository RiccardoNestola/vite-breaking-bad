
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
    <header>
        <nav class="navbar navbar-dark bg-dark">
            <div class="container-fluid">
                <span class="navbar-brand mb-0 h1">YU GI OH</span>
                <p class="navbar-brand mb-0 h1 text-danger">Numbers: {{ store.CharactersList.length }}</p>
            </div>
        </nav>
    </header>
</template>

<style lang="scss" scoped>

</style>