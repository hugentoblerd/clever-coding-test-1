<template>
  <div class="hello">
    <h1 v-if="selectedNumber">The selected number is {{ selectedNumber }}</h1>
    <h1 v-else>None Selected</h1>
    <div class="container">
        <div class="content" v-for="number in numbers" :key="number">
            <button v-on:click="selectedNumber = number">{{ number }}</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['numbers', 'selectedNumber']
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
a {
  color: #42b983;
}
.container {
    display: flex;
    flex-wrap: wrap;
}
.content {
    width: 50px;
}
</style>
