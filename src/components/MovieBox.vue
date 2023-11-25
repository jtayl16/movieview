<template>
    <div v-for="movie of movies" :key="movie.id">
        <SingleMovie :movie=movie />
    </div>
</template>

<script>
import SingleMovie from './SingleMovie.vue'

export default{
    name: 'MovieBox',
    props:{
        movies: Array
    },
    components:{
        SingleMovie
    }
}
</script>

<style scoped>

</style>