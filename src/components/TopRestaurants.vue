<template>
<div v-for="restaurant of restaurants.restaurants" :key="restaurant.id">
    <ResList :restaurant="restaurant" />
</div>
<div>
<Footer/>
</div>
</template>

<script>
import ResList from './ResList.vue'
import Footer from  './Footer.vue'

export default{
    name: 'TopRestaurants',
    props:{
        restaurants:Array
    },
    components:{
        ResList,
        Footer
    }
}
</script>

<style scoped>
</style>