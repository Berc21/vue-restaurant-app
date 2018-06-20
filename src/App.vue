<template>
  <div id="app">
    <ul id="restaurant-list">
    <RestaurantCard/>
    </ul>
  </div>
</template>

<script>
import RestaurantCard from "./components/RestaurantCard.vue";
export default {
  name: "app",
  components: {
    RestaurantCard
  },
  data() {
    return {
      restaurants: []
    };
  },
  methods: {
    getRestaurants(url) {
      fetch(url)
        .then(res => {
        
          return res.json();
        })
        .then(res => {
          console.log(res)
          this.restaurants = res;
        });
    }
  },
  created() {
    const url = "http://localhost:1337/restaurants"
    this.getRestaurants(url);

  }
};
</script>

<style>
#restaurants-list {
  background-color: #f3f3f3;
  list-style: outside none none;
  margin: 0;
  padding: 30px 15px 60px;
  text-align: center;
}
</style>
