
<script>
import axios from 'axios';

import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'

import { store } from './store.js';

export default {
  components:{
    AppHeader,
    AppMain
  },

  data() {
    return {
      store,
    }
  },

  mounted() {
    this.getType()
  },
  methods: {
    getType(){
      let myUrl = store.apiUrl;

      if(store.typeValue !== ''){
        myUrl += `&eq[type1]=${store.typeValue}`;
      }

      axios.get(myUrl).then((response) => {
        store.pokemonList = response.data.docs;
        store.loading = false;
      });

    }
  },
}
</script>
<template>
  <div>
    <AppHeader @typeChange="getType"/>
    <AppMain />
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss'as *;
@use './styles/partials/variables' as *;
  
</style>