<template>
    <div>
    <h1>{{title}}</h1>
    </div>
</template>

<script>

export default{
    name:'MyHeader',
    props:{
        title:String,
    }
}
</script>

<style scoped>
div{
    background-color: #224188;
    color: white;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin-left: 8.4em;
}
</style>