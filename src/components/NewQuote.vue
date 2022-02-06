<template>
    <div>
        <h4>Quote</h4>
        <textarea rows="5" cols="60" v-model="quote"></textarea>
        <button 
            @click="(quotesLength === 10) ? this.alert('Delete a quote to add more!') : addQuote(quote)"
        >
            Add Quote
        </button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            }
        },
        props: {
            addQuote: {
                type: Function,
                required: true
            },
            quotesLength: {
                type: Number,
                required: true
            }
        }
    }
</script>