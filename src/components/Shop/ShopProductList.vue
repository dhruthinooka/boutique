<script setup lang="ts">

import ShopProduct from '@/components/Shop/ShopProduct.vue'
import type { ProductInterface } from '@/interfaces/product.interface.ts'

defineProps<{
  products: ProductInterface[]
}>()

const emit = defineEmits<{
  (e: 'addProductToCart', productId: number): void
}>()

</script>

<template>
  <div class="grid p-20">
    <ShopProduct @add-product-to-cart="emit('addProductToCart', $event)"
                 v-for="product of products" :product="product" />

  </div>
</template>

<style lang="scss" scoped>
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 300px;
  grid-auto-rows: 300px;
  gap: 10px;
}
</style>
