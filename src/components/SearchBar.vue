<template>
  <form>
    <input type="text" placeholder="Search..." />
    <p>
      <input type="checkbox" @change="$emit('showStockedOnly', $event.target.checked)"/>
      Only show products in stock
    </p>
  </form>
</template>

<script>
export default {

}
</script>
