<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
  </div>
</template>
<script>
  import CityHeader from './component/header.vue'
  import CitySearch from './component/search.vue'
  export default {
    name:'City',
    components:{
      CityHeader,
      CitySearch
    }
  }
</script>
<style lang="stylus" scoped>
</style>
