<template>
  <div id="app">
    <h1>Parent {{ pizzaName }}</h1>
    <app-pizza :pizzaName = 'pizzaName' :pizzaPrice="pizzaPrice" :pizzaSize="pizzaSize" @nameChanged = 'pizzaName = $event'> </app-pizza>
    <appCounter ></appCounter>
  </div>
</template>

<script>
import Pizza from './Pizza.vue'
import Counter from './Counter.vue'
export default {
  name: 'app',
  data () {
    return {
      pizzaName: 'Dominos',
      pizzaPrice: "ddd",
    }
  },
  components: {
    appPizza: Pizza,
    appCounter: Counter
  }
}
</script>

