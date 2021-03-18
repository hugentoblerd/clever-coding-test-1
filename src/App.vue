<template>
  <div id="app">
    <NumberSelector :numbers="numbers" :selectedNumber="selectedNumber" @update-number="updateSelected" />
  </div>
</template>

<script>
import NumberSelector from './components/NumberSelector'

export default {
  name: 'App',
  components: {
    NumberSelector
  },
  data () {
    return {
      numbers: [],
      selectedNumber: false
    }
  },
  created: function () {
    let num = 1

    for (let i = 0; i < 100; i++) {
      this.numbers = num++
    }
  },
  methods: {
    updateSelected (newNumber) {
      this.selectedNumber = newNumber
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
