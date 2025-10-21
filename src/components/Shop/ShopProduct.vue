<script setup lang="ts">

</script>

<template>
  <div class="product d-flex flex-column">
    <div class="product-image"></div>
    <div class="p-10 d-flex flex-column">
      <h4>Macbook Pro</h4>
      <p>Lorem ipsum dolor sit amet, consectetur </p>
      <div class="d-flex flex-row align-items-center">
        <strong class="flex-fill">Prix: 1500€</strong>
        <button class="btn btn-primary">Ajouter au panier</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .product {
    background-color: white;
    border: var(--border);
    border-radius: var(--border-radius);
    &-image {
      border-top-right-radius: var(--border-radius);
      border-top-left-radius: var(--border-radius);
      background-image: url(../../assets/macbookpro.jpg);
      background-size: cover;
      background-position: center;
      height: 150px;
    }
  }
</style>
