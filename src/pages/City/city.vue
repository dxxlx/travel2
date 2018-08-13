<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :letter="letter" :cities="cities" :hotCities="hotCities"></city-list>
    <city-alphabet
      :cities="cities"
      @change="handleLetterChange"
    >

    </city-alphabet>
  </div>
</template>
<script>
  import CityHeader from './component/header.vue'
  import CitySearch from './component/search.vue'
  import CityList from './component/List.vue'
  import CityAlphabet from './component/Alphabet.vue'
  import axios from 'axios'
  export default {
    name:'City',
    components:{
      CityHeader,
      CitySearch,
      CityList,
      CityAlphabet
    },
    data(){
      return{
        cities:{},
        hotCities:[],
        letter:''
      }
    },
    methods:{
      getCityInfo(){
        axios.get('/api/city.json')
          .then(this.getCityInfoSucc)
      },
      getCityInfoSucc(res){
        res=res.data
        if(res.ret&&res.data){
          const data=res.data
          this.cities=data.cities
          this.hotCities=data.hotCities
        }
      },
      handleLetterChange(letter){
        this.letter=letter
      }
    },
    mounted(){
      this.getCityInfo()
    }
  }
</script>
<style lang="stylus" scoped>
</style>
