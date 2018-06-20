<template>
    <li>
    <img class="restaurant-img" src="/img/1.jpg">
    <h1>Mission Chinese Food</h1>
    <p>Manhattan</p>
    <p>171 E Broadway, New York, NY 10002</p>
    <a href="./restaurant.html?id=1">View Details</a>
  </li>
</template>

<script>
export default {
  props: {
    restaurants: String,
    required: true,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
