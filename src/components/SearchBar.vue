<template>
  <form>
    <input type="text"
     placeholder="Search..."
     @input="$emit('searchTermUpdated', $event.target.value)"/>
    <p>
      <input type="checkbox"
       @change="$emit('showStockedOnly', $event.target.checked)"/>
      Only show products in stock
    </p>
  </form>
</template>

<script>
export default {

}
</script>
