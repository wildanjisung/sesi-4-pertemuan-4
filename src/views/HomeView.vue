<template>
  <div>
    <CounterComponent @update-counter="updateCounterValue" />
    <h1>angak: {{ angka }}</h1>
  </div>
</template>

<script>
// @ is an alias to /src
import CounterComponent from '../components/CounterComponent.vue'

export default {
  name: 'HomeView',
  components: {
    CounterComponent
  },
  data() {
    return {
      angka: 0
    }
  },
  methods: {
    updateCounterValue() {
      this.angka++
    }
  },
  mounted() {
    console.log(this.angka)
    console.log("updated value at mounted")
    this.updateCounterValue()
    console.log(this.angka)
  }
}
</script>
