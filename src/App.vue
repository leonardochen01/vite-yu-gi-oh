
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
        store.resultArray = result.data.data;
        console.log(result.data.data);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}

</script>

<template>

  <div class="c-header col-12 d-flex px-4">

    <h1>
      Yu-Gi-Oh Api
    </h1>

  </div>

  <div class="c-body pt-3">

    <select id="menu-options" name="options">
      <option value="option-1">Alien</option>
      <option value="option-2">Monster</option>
      <option value="option-3">Magician</option>
      <option value="option-4">Spell</option>
    </select>

    <div class="c-cards col-10 mt-3 pt-3 mx-auto">

      <div class="container mt-4 col-12">
        <cardContainer />
      </div>

    </div>

  </div>


</template>


<style lang="scss">

@use './scss/general.scss';
@import 'bootstrap/scss/bootstrap.scss'

</style>
