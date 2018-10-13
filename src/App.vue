<template>
  <div id="app">
    <table>
      <product-row v-for = "item in items"
            :name="item.name"
            :price="item.price"
            :stocked="item.stocked">
      </product-row>
    </table>
  </div>
</template>

<script>

import ProductRow from './components/ProductRow.vue'
import ProductCategoryRow from './components/ProductCategoryRow.vue'

export default {
  name: 'app',
  components: {
    ProductRow,
    ProductCategoryRow
  },
  data () {
    return {
      items: [
        {category: "Sporting Goods", price: "$49.99", stocked: true, name: "Football"},
        {category: "Sporting Goods", price: "$9.99", stocked: true, name: "Baseball"},
        {category: "Sporting Goods", price: "$29.99", stocked: false, name: "Basketball"},
        {category: "Electronics", price: "$99.99", stocked: true, name: "iPod Touch"},
        {category: "Electronics", price: "$399.99", stocked: false, name: "iPhone 5"},
        {category: "Electronics", price: "$199.99", stocked: true, name: "Nexus 7"}
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
