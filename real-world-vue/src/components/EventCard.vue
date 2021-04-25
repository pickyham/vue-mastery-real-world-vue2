<!-- body part -->
<template>
<!-- Must have 1 root element -->
<!-- event-card : scoped / -shdow : gloabal -->
  <div class="event-card -shadow">
  <router-link class="event-link" :to="{ name: 'event-show', params: { id :'1'}}">
    <span class="eyebrow">@{{event.time}} on {{event.date}}</span>
    <h4 class="title">{{event.title}}</h4>
    <span>{{ event.attendees.length}} attending </span>
  </router-link>
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
       event : {
        id: 1,
        title: 'Beach Cleanup',
        date: 'Tue May 15 2018',
        time: '6:00',
        attendees: [
          { id: 'abc123', name: 'Adam Jahr' },
          { id: 'def456', name: 'Gregg Pollack' }
        ]
       }
      }
    } 
  }
</script>

<!-- clothes (dressed up) -->

<style scoped>
/* scoped means giving style identified to only this component. if not using, the given style in this style will set all over the h4 tags. */
    .event-card {
      padding: 20px;
      margin-bottom: 24px;
      transition: all 0.2s linear;
      cursor: pointer;
    }
    .event-card:hover {
      transform: scale(1.01);
      box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
    }
    .event-card > .title {
      margin: 0;
    }
    
    .event-link {
      color: black;
      text-decoration: none;
      font-weight: 100;
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