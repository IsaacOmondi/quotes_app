<template>
  <div class="row">
    <form style="width:100%">
      <div class="col-sm-8 offset-sm-2 col-xs-12 col-md-6 offset-md-3 form-group">
        <label for="quote">Quote</label>
        <textarea class="form-control" rows="3" v-model="quote" required></textarea>
      </div>

      <div class="col-sm-8 offset-sm-2 col-xs-12 col-md-6 offset-md-3 form-group">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      quote: ""
    };
  },
  methods: {
    createNew() {
      if (this.quote === "") {
          alert("Please enter a quote.");
      } else {
        this.$emit("quoteAdded", this.quote);
        this.quote = "";
      }
    }
  }
};
</script>

<style>
</style>
