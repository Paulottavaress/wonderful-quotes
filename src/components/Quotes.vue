<template>
    <div>    
        <app-quote
            v-for="(quote, index) in quotes"
            :key="index"
        >
            <div @click="deleteQuote(index)">
                <p> {{quote}}</p>
            </div>
        </app-quote>
    </div>
</template>

<script>
import Quote from './Quote.vue'

    export default {
        props: {
            quotes: {
                type: Array
            },
            deleteQuote: {
                type: Function,
                required: true
            }
        },
        components: {
            appQuote: Quote
        }
    }
</script>