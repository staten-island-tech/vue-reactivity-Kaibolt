<template>
  <div v-for="glassItem in glassItems" class="card bg-base-100 w-96 shadow-xl">
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
    name: 'Antique Carnival Glass',
    price: '$1400.50',
    image: '/Glass_Items/3ee25c432c7c4099aa04163907fc100b.webp',
    imgDesc: 'Image Desc1',
  },
  {
    name: 'Antique German Schwarzlot Uranium Glass Vase',
    price: '$995.00',
    image: '/Glass_Items/image-asset.jpeg',
    imgDesc: 'Image Desc2',
  },
  {
    name: 'Decorative Recycled Glass Balls',
    price: '$84.99',
    image: '/Glass_Items/decorative-recycled-glass-balls-m.jpg',
    imgDesc: 'Image Desc2',
  },
]
const metalItems = [
  {
    name: '19th Century Metal Scale',
    price: 'Placeholder Price',
    image:
      '/Metal_Items/19th-century-collection-of-bell-metal-balance-scale-weights_208813_pic1_size3.webp',
    imgDesc: 'Image Desc1',
  },
  {
    name: 'Placeholder Name2',
    price: 'Placeholder Price2',
    image: '/Metal_Items/12856-antique-gilt-metal-desk-set-in-wooden-velvet-lined-case-4-2000x.jpg',
    imgDesc: 'Image Desc2',
  },
]
</script>

<style scoped></style>
