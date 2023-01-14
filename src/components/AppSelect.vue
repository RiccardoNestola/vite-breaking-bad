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

    <div class="col-12 col-md-6 col-lg-3 pt-4 navbar-brand mb-0 d-flex flex-row-reverse py-4">
        <select class="form-select" v-model="store.selectOutput" @change="$emit('onSelect', store.selectOutput)">
            <option value="Alien">Alien</option>
            <option value="Laval">Laval</option>
            <option value="Vylon">Vylon</option>
            <option value="Inzektor">Inzektor</option>
            <option value="Umi">Umi</option>
            <option value="Gusto">Gusto</option>

        </select>
    </div>

</template>

<style lang="scss">

</style>

