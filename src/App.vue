<template>
    <div class="container">
        <app-header :quotesLength="quotes.length"></app-header>
        <app-new-quote :addQuote="addQuote" :quotesLength="quotes.length"></app-new-quote>
        <app-quotes :quotes="quotes" :deleteQuote="deleteQuote"></app-quotes>
        <div>
            <p>Info: Click on a Quote to delete it</p>
        </div>
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
            },
            deleteQuote(quoteIndex) {
                this.quotes.splice(quoteIndex, 1);
            }
        }
    }
</script>

<style scoped>
</style>
