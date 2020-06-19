<template>
  <div>
    <p>组件Two two_number = [{{two_number}}] <button @click="twoNumberAdd">two_number + 1</button></p>
    <div class="three">
      <Three />
    </div>
  </div>
</template>

<script>
import Three from './Three.vue'
export default {
  name: 'Two',
  components: {
    Three
  },
  data() {
    return {
      two_number: 1
    }
  },
  methods: {
    twoNumberAdd() {
      this.two_number += 1;
    }
  },
  updated() {
    console.log('component two update');
  }
}
</script>

<style scoped>
.three {
  margin: 20px;
  border: 1px solid #aaa;
}
</style>
