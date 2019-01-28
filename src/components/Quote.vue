<template>
    <div>
        <div class="title">
            <slot name="title"></slot>
        </div>
        <hr>
        <div>
            <slot name="content"></slot>
        </div>
        <div>
            <slot></slot>
        </div>
        <div style="color: red;">
            <slot name="extra">this is default text</slot>
        </div>
    </div>
</template>

<script>
    export default {
        props:{
            //quote:String,
        }
    }
</script>

<style scoped>
    div{
        border: 1px solid #ccc;
        box-shadow: 1px 1px 5px black;
        padding: 30px;
        margin:30px auto;
        text-align: center;
    }
    h1{
        color: red;
    }
    .title{
        font-style: italic;
    }
</style>