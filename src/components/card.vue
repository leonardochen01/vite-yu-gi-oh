<script>
export default {
  name: 'card',
  props: ['cardData']
}
</script>

<template>

  <img :src="cardData.card_images[0].image_url" alt="">
  <h6>{{ cardData.name }}</h6>
  <p>{{ cardData.type }}</p>


</template>

<style>


</style>