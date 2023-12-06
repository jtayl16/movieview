<template>
  <!-- using boolean class definition -->
  <div :class="movie.id%2 == 0 ? 'pastelgreen':'pastelred' ">
    <img :src="movie.poster" alt="Movie poster">
    <div class="moviedetails">
      <h1 style="">{{movie.title}}</h1>
      <h1>{{movie.year}}</h1>
      <h2>{{movie.tagline}}</h2>
      <h2>Rated {{movie.MPAArating}}</h2>
      <h2>Metascore: {{movie.metascore}}</h2>
    </div>
  </div>
</template>

<script>
export default{
    name: 'SingleMovie',
    props:{
      movie: Object
    }
} 
</script>

<style scoped>
img {
  left: 70%;
  top: 0;
  width: 15em;
  height: 100%;
  position: absolute;
}
.pastelgreen {
  background-color: #77dd77 !important;
}
.pastelred {
  background-color: #ff6961 !important;
}
h2 {
  font-size: 1em;
}
h4 {
  margin: 2px
}
.pastelgreen, .pastelred {
  background-color: #FFB89e;
  color: black;
  padding: 2em;
  text-align: left;
  margin: 1em;
  position: relative;
}
.moviedetails {
  word-wrap: normal;
  max-width: 55vw;
}
</style>
