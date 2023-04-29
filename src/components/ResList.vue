<template>
    <div>
            <h2>{{restaurant.name}}</h2>
            <h4>{{restaurant.description}}</h4>
            <h4>{{restaurant.category}}</h4>
            <h4>{{restaurant.address}}</h4>
            <h4>{{restaurant.openinghours}}</h4>
            <h4><a target="_blank" v-bind:href="restaurant.weburl">{{restaurant.weburl}}</a></h4>
    </div>
</template>

<script>
export default{
    name: 'ResList',
    props:{
        restaurant: Array
    }
}
</script>

<style scoped>
h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
}
</style>