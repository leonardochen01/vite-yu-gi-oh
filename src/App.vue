
<script>
import axios from 'axios';
import { store } from './data/store';
import cardContainer from './components/cardContainer.vue';
export default{
  name: "App",
  components:{
    cardContainer
  },
  methods: {
    getApi(){
      axios.get(store.apiUrl)
      .then(result => {
        store.resultArray = result.data;
        console.log(result.data);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}

</script>

<template>

  <div class="container">
    <cardContainer />
  </div>


</template>


<style lang="scss">

@use './scss/general.scss';
@import 'bootstrap/scss/bootstrap.scss'

</style>
