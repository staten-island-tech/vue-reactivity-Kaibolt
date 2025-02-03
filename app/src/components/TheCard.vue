<template>
  <div>
    <h2 v-for="glassItem in glassItems">{{ glassItem.name }}</h2>
    <h3 v-for="glassItem in glassItems">{{ glassItem.price }}</h3>
    <img v-for="glassItem in glassItems" :src="glassItem.image" />
  </div>
</template>

<script setup>
const glassItems = [
  {
    name: 'Placeholder Name',
    price: 'Placeholder Price',
    image: '/Glass_Items/3ee25c432c7c4099aa04163907fc100b.webp',
    imgDesc: 'Image Desc1',
  },
  {
    name: 'Placeholder Name2',
    price: 'Placeholder Price2',
    image: '/Glass_Items/image-asset.jpeg',
    imgDesc: 'Image Desc2',
  },
]
</script>

<style scoped></style>
