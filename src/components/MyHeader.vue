<template>
    <div>
        <h2>{{headerString}} </h2>
    </div>
</template>

<script>
    export default{
        name: 'MyHeader',
        props:{
            headerString: String
        }
    }
</script>

<style scoped>
    div {
        text-align: center;
    }
</style>
