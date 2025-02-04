<template>
  <div class="card bg-base-100 w-96 shadow-xl">
    <div class="card-body">
      <h2 class="card-title">{{ glassItem.name }}</h2>
      <p>{{ glassItem.price }}</p>
    </div>
    <figure>
      <img :src="glassItem.image" />
    </figure>
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
