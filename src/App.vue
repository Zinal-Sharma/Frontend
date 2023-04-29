<template>
  <!-- Step 3: Must use the component -->
  <MyHeader title="Top 6 Restaurants of USA"/>
  <TopRestaurants :restaurants=restaurants />
</template>

<script>
// Step 1: Import Component 
  import MyHeader from './components/MyHeader.vue'
  import TopRestaurants from  './components/TopRestaurants.vue'

  export default{

    name: 'App',
    // Step 2: You must register the component 
    components:{
      MyHeader,
      TopRestaurants
    },
 
    data(){
      return {
        restaurants: {
          restaurants: []
        }
      }
    },
    methods:{
      async fetchRestaurants(){
        const res = await fetch("https://thoughtful-fedora-fox.cyclic.app/api")
        const data = await res.json()
        console.log("Api data",data)
        this.restaurants.restaurants = data
      }
    },
    async created(){
      this.fetchRestaurants();      
    }
 }
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
 {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}
</style>
