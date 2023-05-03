<script>
export default {
  name: 'card',
  props: ['cardData']
}
</script>

<template>

  <p>{{ cardData.name }}</p>
  <img :src="cardData.card_images[0].image_url" alt="">

</template>

<style>


</style>