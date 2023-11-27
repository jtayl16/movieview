<template>
  <!-- using boolean class definition -->
  <div :class="movie.id%2 == 0 ? 'green':'red' ">
    <h2>{{movie.title}}</h2>
    <h2>{{movie.year}}</h2>
    <h2>{{movie.tagline}}</h2>
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
.green {
  background-color: green;
}
.red {
  background-color: orangered !important;
}
h2 {
  font-size: 1em;
}
h4 {
  margin: 2px
}
div {
  background-color: #FFB89e;
  color: black;
  padding: 1em;
  text-align: center;
  margin: 1em;
}
</style>
