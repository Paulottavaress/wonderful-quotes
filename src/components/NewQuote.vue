<template>
    <div>
        <h4>Quote</h4>
        <textarea rows="5" cols="60" v-model="quote"></textarea>
        <button @click="addQuote">Add Quote</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            }
        },
        methods: {
            addQuote() {
                this.$emit('addQuote', this.quote);
            }
        }
    }
</script>
