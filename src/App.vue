<template>
  <div id="app">
    <ItemList :items="products" />
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue'

export default {
  name: 'App',
  components: {
    ItemList
  },
  data() {
    return {
      products: [
        { name: 'Item 1', price: 10, isVisible: true },
        { name: 'Item 2', price: 20, isVisible: false },
        { name: 'Item 3', price: 15, isVisible: true }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>
