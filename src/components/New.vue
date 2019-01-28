<template>
    <div>
        <h3>New Quote</h3>
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
            console.log('New.vue component Destroyed');
        },
        activated(){
            console.log('New.vue component Activated');
        },
        deactivated(){
            console.log('New.vue component Deactivated');
        }
    }
</script>

<style scoped>

</style>