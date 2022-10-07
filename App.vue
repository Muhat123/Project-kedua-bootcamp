<template>
  <div></div>
  <HelloWorld />
  <div class="container">
    <div class="row">
      <div class="col-8">
        <ProductsList />
        <div class="col-4">
          <CartNew />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ProductsList from './components/ProductsList.vue'
import CartNew from './components/CartNew.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    ProductsList,
    CartNew,
},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c4763;
}
</style>
