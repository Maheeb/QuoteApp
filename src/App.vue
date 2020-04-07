<template>
  <div class="container">
        <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"> </app-header>
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-great :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-great>
      <br><br><br><br><br>
        <div class="row">
                <div class="col-sm-12 text-center">
                    <div class="alert alert-info">

                            Information: To delete a quote just click !!

                    </div>
                </div>

        </div>

  </div>
</template>

<script>
    import  QuoteGreat  from './components/QuoteGreat'
    import  NewQuote  from './components/NewQuote'
    import  Header  from './components/Header'

export default {
  name: 'App',
  components: {
      appQuoteGreat: QuoteGreat,
      appNewQuote: NewQuote,
      appHeader: Header
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

            if(this.quotes.length>=this.maxQuotes){
                alert('Please delete some quotes')
            }
            this.quotes.push(quote)
        },
        deleteQuote: function (index) {

            this.quotes.splice(index,1);

        }
      
    }

}
</script>

<style>

</style>
