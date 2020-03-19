<template>
  <div id="app">
    <coffee-roulette :staff="staff" :coffeeMaker="coffeeMaker"></coffee-roulette>
    <button class="roulette-button" v-on:click="spinRoulette">Spin</button>
    <div class="chosen-staff">{{ coffeeMaker }}</div>
  </div>
</template>

<script>
import CoffeeRoulette from './components/CoffeeRoulette.vue'

export default {
  name: 'app',
  components: {
    CoffeeRoulette
  },
  data() {
    return {
      staff: [{
        name: 'Joe',
      }, {
        name: 'Tom',
      }, {
        name: 'Martin',
      }, {
        name: 'Alice',
      }, {
        name: 'Bret',
      }, {
        name: 'Claire',
      }, {
        name: 'Dan',
      }, {
        name: 'Richard',
      }],
      coffeeMaker: ''
    };
  },
  methods: {
    spinRoulette: function(event) {
      const idx = Math.floor(Math.random() * this.staff.length);
      if (event) {
        this.coffeeMaker = this.staff[idx]['name'];
      }
    }
  }
};
</script>
