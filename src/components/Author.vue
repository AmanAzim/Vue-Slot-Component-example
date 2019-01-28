<template>
    <div>
        <h1>Author</h1>
        <button @click="counter++">Increment</button>
        <p>Counter: {{counter}}</p>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                counter:0
            };
        },
        destroyed() {
            console.log('Author.vue component Destroyed');
        },
        activated(){
            console.log('Author.vue component Activated');
        },
        deactivated(){
            console.log('Author.vue component Deactivated');
        }

    }
</script>

<style scoped>

</style>