<!-- body part -->
<template>
<!-- Must have 1 root element -->
  <div id="nav">
      <router-link :to="{ name: 'event-list' }">LIST</router-link> |
      <router-link :to="{ name: 'event-create' }">Create</router-link>
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
<style scoped> 
/* scoped means giving style identified to only this component. if not using, the given style in this style will set all over the h4 tags. */
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<!-- each tags set property 'lang' 
but there is a caveat. 
there is a list to avoid it.
1. Setup Preloaders
2. Configure Webpack

Check which dependencies are needed in the doc
https://vue-loader.vuejs.org/guide/pre-processors.html
-->