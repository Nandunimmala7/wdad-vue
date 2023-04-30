<template>
  <MyHeader />
  <MyPizza :pizzaDetails="pizzas" />
</template>

<script>
import MyHeader from "./MyHeader.vue";
import MyPizza from "./MyPizza.vue";

export default {
  name: "MyHome",
  components: {
    MyHeader,
    MyPizza,
  },
  data() {
    return {
      pizzas: [],
    };
  },
  mounted() {
    this.fetchPizzas();
  },
  methods: {
    fetchPizzas() {
      fetch("https://wdad-node.herokuapp.com/api/getPizzas")
        .then((response) => response.json())
        .then((data) => {
          this.pizzas = data;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  height: 54px;
  background-color: black;
  color: white;
}
</style>
