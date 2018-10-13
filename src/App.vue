<template>
  <div id="app">
    <search-bar></search-bar>
    <product-table :items="items"></product-table>
  </div>
</template>

<script>

import ProductTable from './components/ProductTable.vue'
import SearchBar from './components/SearchBar.vue'
export default {
  name: 'app',
  components: {
    ProductTable,
    SearchBar
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

table {
  width: 50%;
  height: 100%;
  border: 3px black double;
  margin: 0 auto;
}

.category-header {
  text-decoration: underline;
}
</style>
