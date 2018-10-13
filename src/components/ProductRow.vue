<template>
    <tr>
        <td> <span :style="{color: this.color }"> {{ this.name }}</span> </td>
        <td> {{ price }} </td>
    </tr>
</template>

<script>
export default {
  props: ['name', 'price', 'stocked'],
  computed: {
    color() {
      return this.stocked ? "black" : "red"
    }
  }
}
</script>
