<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <label>Quote</label>
                <textarea class="form-control" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <button 
                    class="btn btn-primary"
                    @click.prevent="newQuote()"
                >
                    Add Quote
                </button>
            </div>
        </form>
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
            newQuote() {
                this.quotesLength === 10
                    ? this.alert('Delete a quote to add more!')
                    : this.addQuote(this.quote);
                this.quote = '';
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