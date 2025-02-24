<template>
  <div class="flex m-16">
    <div class="cart m-8">
      <h3>Cart</h3>
      <ul>
        <div class="card glass w-96 m-4" v-for="(item, index) in cart" :key="index">
          <div class="card-body">
            <h2 class="card-title">{{ item.name }}</h2>
            <p>Quantity: {{ item.quantity }} , Price per Item: ${{ item.price }}</p>
            <button @click="removeFromCart(item)" class="btn btn-primary">Remove</button>
          </div>
        </div>
      </ul>
      <p>Total: ${{ totalPrice }}</p>
      <p>Total Items: {{ totalItems }}</p>
    </div>

    <TheCard :addToCart="addToCart" />
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'
import { allItems } from '@/assets/allItems.js'
import TheCard from './TheCard.vue'

const cart = reactive([])
const totalItems = ref(0)
const totalPrice = ref(0)

const addToCart = (item) => {
  const existingItem = cart.find((cartItem) => cartItem.name === item.name)
  if (existingItem) {
    existingItem.quantity += 1
  } else {
    cart.push({ ...item, quantity: 1 })
  }
  updateCart()
}

const removeFromCart = (item) => {
  const existingItem = cart.find((cartItem) => cartItem.name === item.name)

  if (existingItem) {
    if (existingItem.quantity > 1) {
      existingItem.quantity -= 1
    } else {
      const index = cart.findIndex((cartItem) => cartItem.name === item.name)
      if (index !== -1) {
        cart.splice(index, 1)
      }
    }
  }
  updateCart()
}

const updateCart = () => {
  totalItems.value = cart.reduce((sum, item) => sum + item.quantity, 0)
  totalPrice.value = cart.reduce((sum, item) => sum + item.price * item.quantity, 0)
}
</script>

<style scoped></style>
