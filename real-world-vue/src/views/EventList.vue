<template>
<div>
  <h1>Events Listing</h1>
  <router-link :to="{ name: 'event-show', params: { id :'1'}}" class="block" >Show Event #1</router-link>
  <router-link :to="{ name: 'event-show', params: { id :'2'}}" class="block">Show Event #2</router-link>
  <router-link :to="{ name: 'event-show', params: { id :'3'}}" class="block">Show Event #3</router-link>
</div>
</template>

<script>
export default {

}
</script>

<style>
.block{
    display: block;
}
</style>