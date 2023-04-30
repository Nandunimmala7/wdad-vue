<template>
  <div class="card">
    <div class="container">
      <div>Name: {{ pizzaData.name }}</div>
      <div>Size: {{ pizzaData.size }}</div>
      <div>Price: {{ pizzaData.price }}</div>
      <div>Average Review: {{ pizzaData.avgReview }}</div>
      <div>Toppings : {{ pizzaData.toppings + "" }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PizzaCard",
  props: {
    pizzaData: Object,
  },
};
</script>

<style scoped>
.card {
  background-color: #ffffff;

  box-shadow: 0 4px 8px 0 rgba(252, 245, 245, 0.2);
  transition: 0.3s;
  width: 100%;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

.container {
  padding: 2px 16px;
}
</style>
