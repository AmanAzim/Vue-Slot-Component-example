<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <button @click="selectedComponent='app-quote'">Quote</button>
                <button @click="selectedComponent='app-author'">Author</button>
                <button @click="selectedComponent='app-new'">New</button>

                <p>{{selectedComponent}}</p>

                <component :is="selectedComponent"> <p>default component</p> </component>
                <hr>

                <keep-alive>
                <component :is="selectedComponent"> <p>default component</p> </component>
                </keep-alive>

              <!-- <app-quote>

                   <h1 slot="title">{{parentQuote}}</h1>
                   <p slot="content">A wonderful Quote</p>
                   <p>Second wonderful quote</p>
                   <p slot="extra">Extra wonderful quote</p>

               </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'
    import Author from './components/Author.vue'
    import New from './components/New.vue'

    export default {
        components:{
            'app-quote':Quote,
            'app-author':Author,
            'app-new':New,
        },
        data(){
            return{
                parentQuote:'The Quote',
                selectedComponent:'app-quote',
            };
        }
    }
</script>

<style>
    h1{
        color: green;
    }
</style>
