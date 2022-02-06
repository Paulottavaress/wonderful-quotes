<template>
    <div class="container">
        <app-header :quotesLength="quotes.length"></app-header>
        <app-new-quote @addQuote="addQuote"></app-new-quote>
        <app-quotes></app-quotes>
    </div>
</template>

<script>
import Header from './components/Header.vue';
import NewQuote from './components/NewQuote.vue';
import Quotes from './components/Quotes.vue';

    export default {
        data() {
            return {
                quotes: []
            }
        },
        components: {
            appHeader: Header,
            appNewQuote: NewQuote,
            appQuotes: Quotes,
        },
        methods: {
            addQuote(quote) {
                this.quotes.push(quote);
                console.log(this.quotes);
            }
        }
    }
</script>

<style>
</style>
