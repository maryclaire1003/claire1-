<template>
  <div>
    <h1>Item List</h1>
    <div v-for="(item, index) in filteredItems" :key="index">
      <Item :item="item" @add-to-cart="handleAddToCart" />
    </div>
  </div>
</template>

<script>
import Item from 'Item.vue'

export default {
  name: 'ItemList',
  components: {
    Item
  },
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  computed: {
    filteredItems() {
      return this.items.filter((item) => item.isVisible)
    }
  },
  methods: {
    handleAddToCart(item) {
      console.log(`Addedtocart: ${item.name} - $${item.price}`)
    }
  }
}
</script>

<style scoped>
h1 {
  color: #333;
}
</style>
