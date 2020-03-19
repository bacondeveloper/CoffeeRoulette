<template>
  <div class="coffee-roulette">
    <h1>Coffee Roulette</h1>
    <div class="staff-card-container">
      <div class="staff-card" v-for="(staf, index) in staff" :key="index">
        <h3>{{ staf.name }} </h3>
      </div>
    </div>
  </div>
</template>

<script type="text/javascript">
  export default {
    props: ['staff', 'coffeeMaker']
  };
</script>
