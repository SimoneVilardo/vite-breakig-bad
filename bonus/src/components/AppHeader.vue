<script>
import { store } from '../store.js';
import AppSelect from './AppSelect.vue'

export default {
    components:{
        AppSelect
    },
    data() {
        return {
            store
        }
    },    
}
</script>
<template>
    <div class="container">
        <div class="row">
            <div class="col-4 d-flex ">
                <div class="water-circ m-2"></div>
                <div class="fire-circ m-2"></div>
                <div class="electric-circ m-2"></div>
                <div class="grass-circ m-2"></div>
            </div>
            <div class="col-4">
                <div class="text-center stile">
                    {{ store.titleApp }}
                    
                </div>
            </div>
            <div class="col-4">
                <AppSelect />
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .stile{
        color: white;
        font-size: 30px;
        font-weight: bold;
    }

    .fire-circ, .electric-circ, .grass-circ {
        height: 40px;
        width: 40px;
        border-radius: 50%;
        border: 4px solid white;
    }
    
    .electric-circ{
        background: rgb(226,240,0);
        background: linear-gradient(297deg, rgba(226,240,0,1) 28%, rgba(255,255,255,1) 90%);
    }

    .water-circ{
        height: 80px;
        width: 80px;
        border-radius: 50%;
        border: 4px solid white;
        background: rgb(0,45,240);
        background: linear-gradient(297deg, rgba(0,45,240,1) 28%, rgba(255,255,255,1) 100%);
    }

    .grass-circ{
        background: rgb(12,175,11);
        background: linear-gradient(297deg, rgba(12,175,11,1) 28%, rgba(255,255,255,1) 90%);
    }

    .fire-circ{
        background: rgb(240,0,0);
        background: linear-gradient(297deg, rgba(240,0,0,1) 28%, rgba(255,255,255,1) 90%);
    }
</style>