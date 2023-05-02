<script>
import { store } from '../data/store'
import card from './card.vue'
export default {
  name: 'cardContainer',
  components:{
    card
  },
  data(){
    return{
      store
    }
  }
}
</script>

<template>

  <div class="c-cards">

    <div v-for="(cardObj, index) in store.resultArray" :key="index">
      <card :cardData="cardObj"/>
      <p>{{ cardObj.name }}</p>
    </div>

  </div>

</template>

<style lang="scss" scoped>

</style>