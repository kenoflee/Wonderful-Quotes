<template>
    <div class="container">
        <app-quote-card :quotes="quotes"></app-quote-card>
    </div>
</template>

<script>
    import QuoteCard from './components/QuoteCard.vue';

    export default {
        data() {
            return {
                quotes: ['How do you like them apple?'],
                maxQuotes: 10,
            }
        },
        components: {
            appQuoteCard: QuoteCard,
        }
    }
</script>

<style>
</style>
