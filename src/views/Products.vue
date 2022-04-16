<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
       <ProductCard
        v-for="(product, index) in inventory.slice(0, 6)"
        :key="product.id"
        :product="product"
        :addToCart="addToCart"
        :index="index"
        class="card"
      />
    </div>
  </main>
</template>

<script>
import ProductCard from "@/components/ProductCard.vue"

export default {
  props: ["inventory", "addToCart"],
  components: {
    ProductCard
  }
}
</script>