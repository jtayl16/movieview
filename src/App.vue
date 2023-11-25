<template>
  <!-- Step 3: use the component -->
  <MyHeader headerString="MovieView" />
  <MovieBox :movies=movies />
</template>

<script>
// Step 1 : you import the component
import MyHeader from './components/MyHeader.vue'  // page header
import MovieBox from './components/MovieBox.vue'  // display movies from JSON

export default{
  name: 'App',
  // Step 2: register the component
  components:{
    MyHeader,
    MovieBox 
  },
  data(){
    return {
      movies: []  // retrieved JSON file
    }
  },
  methods:{
    async fetchmovies(){
      const res = await fetch("http://localhost:3939/movies")
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
    this.movies = await this.fetchmovies()
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
