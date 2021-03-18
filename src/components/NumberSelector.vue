<template>
  <div class="hello">
    <h1 v-if="selectedNumber">The selected number is {{ selectedNumber }}</h1>
    <h1 v-else>None Selected</h1>

    <div class="container">
      <NumberButton v-for="number in numbers" @update-number="$emit('update-number', number)" :key="number" :number="number" />
    </div>
  </div>
</template>

<script>
import NumberButton from './NumberButton'

export default {
  props: ['numbers', 'selectedNumber'],
  components: {
    NumberButton
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
.container {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    margin: 0 20px;
}

/* --- Tablets --- */
@media only screen and (min-width: 768px) and (max-width: 1199px) {
  .container {
    grid-template-columns: repeat(10, 1fr);
    margin: 0 50px;
  }
}

/* --- Desktop --- */
@media only screen and (min-width: 1200px) {
  .container {
    grid-template-columns: repeat(20, 1fr);
    margin: 0 50px;
  }
}
</style>
