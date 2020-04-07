<template>
    <div class="row">

        <appQuote v-for="(quote,index) in quotes" v-bind:index="index" v-bind:quote="quote" v-bind:key="quote.id" >
                {{quote}}

        </appQuote>

    </div>
</template>

<script>
    import Quote from '../components/Quote'
    export default {
        name: "QuoteGreat",
        props:['quotes'],
        components: {

            appQuote: Quote
        }

    }
</script>

<style scoped>

</style>