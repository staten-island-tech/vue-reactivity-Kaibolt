<template>
  <div>
    <h2>{{ glassItems.name }}</h2>
    <h3>{{ glassItems.price }}</h3>
  </div>
</template>

<script setup>
const glassItems = [
  {
    name: 'Placeholder Name',
    price: 'Placeholder Price',
    image: '@/public/Glass_Items/3ee25c432c7c4099aa04163907fc100b.webp',
  },
  {
    //
    name: 'Placeholder Name2',
    price: 'Placeholder Price2',
    image: '@/public/Glass_Items/image-asset.jpeg',
  },
]
</script>

<style scoped></style>
