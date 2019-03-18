<template>
  <div class="header">
    <h1>Quotes Added</h1>

    <div class="progress" style="height: 25px; margin-bottom:10px;">
      <div class="progress-bar" :style="{width:quoteCount*10+'%'}">{{quoteCount}}/{{maxQuotes}} </div>
    </div>

    <div>
  </div>
  </div>
  
</template>

<script>
export default {
  props: ['quoteCount','maxQuotes']
};
</script>

<style scoped>
    div.header {
        margin: 2rem 0;
        width: 100%
    }
</style>
