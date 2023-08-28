<template>
  <div>
    <button @click="doIncrement">counter</button>
  </div>
</template>

<script>
export default {
  name: 'CounterComponent',
  methods: {
    doIncrement() {
      this.$emit("update-counter")
    }
  }
}
</script>
