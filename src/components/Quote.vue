<template>
  <div>
      <div class="title">
        <slot name="title">
        </slot>
        <span style="color: lightblue">
            <!-- if this slot doesn't assign in the app  -->
            <!-- the context between attribute will show  -->
            <!-- however, if the slot is assigned in the app  -->
            <!-- it the context between attribute will be replaced -->
            <slot name="subtitle">
                HERE IS A TEST FOR SLOT WHICH DOESN'T ASSIGN IN THE APP 
            </slot>    
        </span>
      </div>
      <hr>
      <div>
        <slot name="content">
        </slot>    
      </div>
      <div>
          <slot></slot>
      </div>
  </div>
</template>
<script>
export default {
  
}
</script>
<style scoped>
/* must be scoped */
div{
    border:1px solid lightblue;
    box-shadow: 1px 1px 2px black;
    padding: 30px;
    margin: 30px auto;
}
p{
    color:blue
}
.title {
    font-style: italic
}
</style>
