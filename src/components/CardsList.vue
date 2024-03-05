<script>
import {store} from '../store.js';

import CardsItem from './CardItem.vue';

export default {

    name: 'CardsList',

    data() {
        return {
            store,
        }
    },

    components: {
        CardsItem,
    }
}

</script>

<template>
    <h2>
        cards
    </h2>

    <ul>
        <CardsItem v-for="currentcard in store.cards" :card="currentcard" :key="currentcard" ></CardsItem>

    </ul>
    
  
  
</template>

<style lang="scss" >

</style>