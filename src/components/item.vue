<template>
  <div v-if="item.isVisible">
    <h2>{{ item.name }}</h2>
    <p>Price: ${{ item.price }}</p>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script>
export default {
  name: 'item',
  props: {
    item: {
      type: Object,
      required: true
    }
  },
  methods: {
    addToCart() {
      this.$emit('add-to-cart', this.item)
    }
  }
}
</script>

<style scoped>
h2 {
  color: blue;
}
button {
  background-color: green;
  color: white;
  padding: 5px 10px;
  border: none;
  cursor: pointer;
}
</style>
