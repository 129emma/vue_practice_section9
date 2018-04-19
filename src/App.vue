<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <button @click="selectedComponent = 'appQuote'">Quote</button>
        <button @click="selectedComponent = 'appAuthor'">Author</button>
        <button @click="selectedComponent = 'appNew'">New Quote</button>
        
        <p>
          {{ selectedComponent }}
        </p>

        <!-- this component is bond to the selectedComponent property -->
        <!-- and the default value is appQuote -->
        <component :is="selectedComponent">
          <p>Default content</p>
        </component>  


        <!-- <app-Quote> -->
          <!-- use slot = "" can direct to different slot part -->
          <!-- this attribute is implemented by vue.js -->
          <!-- <h1 slot="title">{{ quoteTitle }}</h1>
          <h1 slot="content">slot content shows here</h1> -->
          <!-- another way is remove one of slot name in app and quote  -->
          <!-- it will become unnamed slot -->
          <!-- vue js will detect it as default slot -->
          <!-- and attribute in here without slot will be assigned to the unnamed slot -->
          <!-- as default slot -->
          <!-- <h2>This is for unname slot</h2> -->
        <!-- </app-Quote> -->
      </div>
    </div>
  </div>

</template>

<script>

import Quote from './components/Quote.vue';
import Author from'./components/Author.vue';
import New from './components/New.vue';


export default {
  // even we passing app component to the child component, but if we write other vue syntax in there, it still work.
  // only except style part.
  data: function () {
    return {
      quoteTitle: 'This is added by data!',
      // the default content before click button
      // it assigns appQuote as the default component
      selectedComponent: 'app-Quote'
    }
  },
  components:{
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  }
  
}
</script>

<style>
/* once use slot attribute, if add styling of child component in there, it won't work, it only pass from its own component */

</style>