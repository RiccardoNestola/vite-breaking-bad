<script>
import { store } from "../store"
export default {

    components: {
    },

    data() {
        return {
            store,

        }
    }

}
</script>

<template>
    <div class="row-col-12">

        <input type="text" name="" id="" placeholder="Cerca" v-model="store.textOutput"
            @keyup.enter="$emit('inputSearch', store.textOutput)">

    </div>

</template>


<style lang="scss">

</style>