<script>
import AppCharacterCards from './AppCharacterCards.vue'

import { store } from '../store.js';

export default {
    components:{
        AppCharacterCards
    },
    data() {
        return {
            store
        }
    }
}
</script>
<template>
    <div class="container d-flex justify-content-center align-items-center rounded-5 px-4 py-5 bg-white ">
        <div class="row d-flex justify-content-center col-12 bg-secondary py-2 px-1 overflow-auto high">
            <div v-for="(pokemon, index) in store.pokemonList" :key="index" class="col-6 col-md-4 col-lg-3 min">
                <AppCharacterCards :myPokemon="pokemon" />
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .min{
        min-width: fit-content;
    }

    .high{
        height: 500px;
    }
</style>