<template>
  <div class="container">
    <app-progress-bar :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-progress-bar>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";
import ProgressBar from "./components/ProgressBar.vue";

export default {
  data: function() {
    return {
      maxQuotes: 10,
      quotes: ["Just a quote"]
    };
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appProgressBar: ProgressBar
  },
  methods: {
    newQuote(quote) {
      console.log(this.quotes.length)
      if (this.quotes.length >= this.maxQuotes) {
        alert("Only 10 quotes are allowed");
      } else {
        this.quotes.push(quote);
      }
    },
    deleteQuote(index) {
      this.quotes.splice(index, 1);
    }
  }
};
</script>

<style>
</style>
