
<!-- Task
[ v ] 1. Add Global styles
[ v ] 2. Flesh out EventCard.vue
[ v ] 3. Create Navbar.vue component -->

<template>
<div class="event-list">
  <h1>Events Listing</h1>
    <!-- ES 6 shorthand 
     EventCard : EventCard -->
    <EventCard />
  <router-link :to="{ name: 'event-show', params: { id :'1'}}" class="block" >Show Event #1</router-link>
  <router-link :to="{ name: 'event-show', params: { id :'2'}}" class="block">Show Event #2</router-link>
  <router-link :to="{ name: 'event-show', params: { id :'3'}}" class="block">Show Event #3</router-link>
</div>
</template>

<script>
//vimport (snippet)
import EventCard from '@/components/EventCard.vue';

export default {
    //vcomponents
    components: {
        //put it here to use it as a child component.
        EventCard
    },
}
</script>

<style>
.block{
    display: block;
}
h1{
    color : red
}
.event-list {
    margin : 0 auto;
}
</style>

