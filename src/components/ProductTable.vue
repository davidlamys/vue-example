<template>
  <table>
        <thead>
          <tr>
            <th>Name</th>
            <th>Price</th>
          </tr>
        </thead>
        <tbody v-for="category in categories">
          <product-category-row :category="category">
          </product-category-row>
          <product-row v-for="item in itemsForCategory(category)"
          :name="item.name"
          :price="item.price"
          :stocked="item.stocked">
          </product-row>
        </tbody>
  </table>
</template>

<script>
import ProductRow from './ProductRow.vue'
import ProductCategoryRow from './ProductCategoryRow.vue'

export default {
  components: {
    ProductRow,
    ProductCategoryRow
  },
  props: ["items"],
  computed: {
    categories() {
      const categories = this.items.map((product) => {
        return product.category
      })
      return [...new Set(categories)]
    },
  },
  methods: {
    itemsForCategory(category) {
      return this.items.filter((product) => {
        return product.category == category
      })
    }
  }
}
</script>
