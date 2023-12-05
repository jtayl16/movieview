<template>
  <MyHeader headerString="MovieView" />
  <MovieBox :movies=movies />
</template>

<script>
import MyHeader from './components/MyHeader.vue'  // page header
import MovieBox from './components/MovieBox.vue'  // display movies from JSON

export default{
  name: 'App',
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
      const res = await fetch("https://movieview-backend.onrender.com/api")
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
