<template>
    <div class="card">
        v-for="item in products" :key="item.id">
  <h4 class="card-header">Products</h4>
  <div class="card-body">
    <p class="card-title">Silver Queen</p>
    <p class="card-cost">$0.95</p>
    <a href="#" @click="addToCart(item)" class="btn btn-primary">Add to cart</a>
  </div>
</div>
  <div class="card">
  <div class="card-body">
    <p class="card-title">Snickers</p>
    <p class="card-cost">$0.99</p>
    <a href="#" @click="addToCart(item)" class="btn btn-primary">Add to cart</a>
  </div>
</div>
  <div>
  <div class="card">
  <div class="card-body">
    <p class="card-title"></p>
    <p class="card-text">Dairy Milk</p>
    <p class="card-cost">$1</p>
    <a href="#" @click="addToCart(item)" class="btn btn-primary">Add to cart</a>
  </div>
</div>
</div>
<div>
</div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';

    export default {
        name: "ListProducts",
        computed: {
            ...mapGetters (["products"]),
        },
        methods: {
            ...mapActions (["getProducts", "addToCart"]),
        },
        mounted() {
            this.getProducts();
        }
    };
</script>
<style scoped>
    .card {
        padding-inline-end: 0px;
    }
</style>