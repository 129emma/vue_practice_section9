<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <app-Quote>
          <p>yes I made it!</p>
        </app-Quote>
      </div>
    </div>
  </div>

</template>

<script>

import Quote from './components/Quote.vue';
export default {
  components:{
    appQuote: Quote
  }
  
}
</script>

<style>
