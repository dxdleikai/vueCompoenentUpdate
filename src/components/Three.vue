<template>
  <div>
    <p>组件Three three_number = [{{three_number}}] <button @click="threeNumberAdd">three_number + 1</button></p>
  </div>
</template>

<script>
export default {
  name: 'Three',
  data() {
    return {
      three_number: 1
    }
  },
  methods: {
    threeNumberAdd() {
      this.three_number += 1;
    }
  },
  updated() {
    console.log('component three update');
  }
}
</script>

<style scoped>

</style>
