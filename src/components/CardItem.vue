<script>

export default {

    name: 'CardsItem',

    
    props: {
        card: {
            type: Object,
            
        }
    }   
}

</script>

<template>
    <li>
        <img :src="card.card_images[0].image_url_small" :alt="card.name">
        <h3>{{card.name}}</h3>
        <span>{{ card.archetype }}</span>
    </li>

    
  
</template>

<style lang="scss" >

</style>