<script>
import axios from 'axios';
import {store} from './store.js';


import CardsList from './components/CardsList.vue';

export default {
 data() {
   return {

     store,
   }
  },

  components: {
    CardsList,
  },

   created() {

    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(response => {
      this.store.cards = response.data.data;
    });
    
   },
 

}

</script>

<template>
  <div class="container">
    <CardsList></CardsList>

  </div>
  
</template>

<style lang="scss" >

</style>
