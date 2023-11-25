<template>
    <!-- <div :class="movie.published ? 'green': 'red' "> 
          this chooses a class based off a boolean
    -->
    <div class="green">
      <h2>{{movie.title}}</h2>
      <h2>{{movie.year}}</h2>
    </div>
</template>

<script>
export default{
    name: 'SingleMovie',
    props:{
      movie: Array
    }
} 
</script>

<style scoped>
.green {
  background-color: green;
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
.red {
  background-color: orangered !important;
}
</style>
