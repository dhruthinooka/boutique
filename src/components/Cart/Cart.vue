<script setup lang="ts">

import CartProductList from '@/components/Cart/CartProductList.vue'
import type { ProductCartInterface } from '@/interfaces'

defineProps<{
  cart: ProductCartInterface[]
}>()

const emit = defineEmits<{
  (e: 'removeProductFromCart', productId: number): void
}>()

</script>

<template>
  <div>
    <h2 class="mb-10">Cart</h2>
    <CartProductList :cart="cart"
                     @remove-product-from-cart="emit('removeProductFromCart', $event)"/>
  </div>
</template>

<style lang="scss" scoped>

</style>
