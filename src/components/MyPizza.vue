<template>
  <div class="pizza-card">
    <div v-for="pizza in pizzaDetails" :key="pizza.id">
      <div class="card">
        <pizzaCard :pizzaData="pizza" />
      </div>
    </div>
  </div>
</template>

<script>
import pizzaCard from "./PizzaCard.vue";

export default {
  name: "MyPizza",
  components: {
    pizzaCard,
  },
  props: {
    pizzaDetails: Object,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.pizza-card {
  margin-top: 20px;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  gap: 10px;
}
.card {
  flex: 0 1 30%;
  max-width: 350px;
  min-width: 300px;

  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
