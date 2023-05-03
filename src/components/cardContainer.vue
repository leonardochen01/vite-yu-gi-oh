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

  <div class="c-card d-flex flex-wrap gap-3">

    <div v-for="(cardObj, index) in store.resultArray" :key="index"
    id="c-card">
      <card :cardData="cardObj"/>
    </div>

  </div>

</template>

<style lang="scss" scoped>

</style>