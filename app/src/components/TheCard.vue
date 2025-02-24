<script setup>
import { allItems } from '@/assets/allItems.js'

const cartBase = defineProps({
  addToCart: Function,
})
const cartBuy = (item) => cartBase.addToCart(item) //If this doesn't work, I'm going to be very sad.
</script>
<template>
  <div v-for="allItem in allItems" class="card bg-base-100 w-96 shadow-xl">
    <div class="card-body">
      <h2 class="card-title">{{ allItem.name }}</h2>
      <p>Price: {{ allItem.price }} | Category: {{ allItem.category }}</p>
    </div>
    <figure>
      <img :src="allItem.image" />
    </figure>
    <br />
    <div class="card-actions justify-center">
      <button @click="cartBuy(allItem)" class="btn btn-primary">Buy Now</button>
    </div>
    <br />
  </div>
</template>

<style scoped></style>
