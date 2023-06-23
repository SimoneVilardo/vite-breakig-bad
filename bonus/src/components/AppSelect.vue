<script>
import { store } from '../store.js'

export default {
    data() {
        return {
            store,
            typePokemon: [
                "Bug",
                "Dark",
                "Dragon",
                "Electric",
                "Fairy",
                "Fighting",
                "Fire",
                "Flying",
                "Ghost",
                "Grass",
                "Ground",
                "Ice",
                "Normal",
                "Poison",
                "Psychic",
                "Rock",
                "Steel",
                "Water"
            ]

        }
    },
}
</script>
<template>
    <div>
        <select class="" v-model="store.typeValue">
            <option value="" selected>Select Type</option>
            <option v-for="(type, index) in typePokemon" :key="index" :value="type">{{ type }}</option>
        </select>
    </div>
</template>
<style lang="scss" scoped>
    
</style>