<template>
  <div id="app">
  <div>
    <label>principal capital</label>
    <input v-model.number="principal">
  </div>
  <div>
    <label>Yearly interestRate</label>
    <input v-model.number="interestRate">
  </div>
  <div>
    <label>Investment length (timeYears)</label>
    <input v-model.number="timeYears">
  </div>
  <div>
    You will gain:
    <output>{{final}}</output>
  </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      principal: 0,
      interestRate: 0,
      timeYears: 0
    }
  },
  computed: {
    final () {
      const P = this.principal
      const r = this.interestRate
      const t = this.timeYears
      return P * Math.pow((1 + r), t)
    }
  }
}
</script>
<style>
</style>
