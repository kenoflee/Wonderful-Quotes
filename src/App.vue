<template>
    <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-card :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-card>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">
                    Info: Click on a Quote to delete it!
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import QuoteCard from './components/QuoteCard.vue';
    import NewQuote from './components/NewQuote.vue';

    export default {
        data() {
            return {
                quotes: ['How do you like them apple?', 'I see dead people.'],
                maxQuotes: 10,
            }
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote);
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        },
        components: {
            appQuoteCard: QuoteCard,
            appNewQuote: NewQuote,
        }
    }
</script>

<style>
</style>
