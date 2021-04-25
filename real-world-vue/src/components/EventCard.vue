<!-- body part -->
<template>
<!-- Must have 1 root element -->
  <div>
    <h4>{{title}}</h4>
  </div>
</template>

<!-- brain -->
<script>
  export default {
    // es6 shorthand
    // also looks like this : 
    //data : function(){...}
    data(){
      return{
        title : 'Park Cleanup'
      }
    } 
  }
</script>

<!-- clothes (dressed up) -->
<style lang="scss" scoped>

</style>

<!-- each tags set property 'lang' 
but there is a caveat. 
there is a list to avoid it.
1. Setup Preloaders
2. Configure Webpack

Check which dependencies are needed in the doc
https://vue-loader.vuejs.org/guide/pre-processors.html
-->