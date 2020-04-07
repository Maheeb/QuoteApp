<template>
  <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-great :quotes="quotes"></app-quote-great>
  </div>
</template>

<script>
    import  QuoteGreat  from './components/QuoteGreat'
    import  NewQuote  from './components/NewQuote'
export default {
  name: 'App',
  components: {
      appQuoteGreat: QuoteGreat,
      appNewQuote: NewQuote
  },
    data: function () {
        return{

            quotes:[
                "This is my first quote"
            ],
            maxQuotes:10
        }

    },
    methods:{
        newQuote: function (quote) {
            this.quotes.push(quote)
        }
      
    }

}
</script>

<style>

</style>
