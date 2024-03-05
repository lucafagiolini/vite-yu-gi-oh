<script>
import axios from 'axios';
import {store} from './store.js';

export default {
 data() {
   return {

     store,
   }
  },

   created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then(response => {
      console.log(response.data.data); 
      this.store.cards = response.data.data;
    });
    
   },
 

}

</script>

<template>
  hello
  
</template>

<style lang="scss" >

</style>
