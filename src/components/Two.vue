<template>
  <div>
     <p>接收的props[userName]: {{userName}}</p>
    <p>组件Two two_number = [{{two_number}}] <button @click="twoNumberAdd">two_number + 1</button>
    <button @click="emitData">emitData</button></p>
    <div class="three">
      <Three />
    </div>
  </div>
</template>

<script>
import Three from './Three.vue'
export default {
  name: 'Two',
  props: ['userName'],
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
    },
    emitData() {
      this.$emit('newName', 'jarry');
    }
  },
  updated() {
    console.log('component two update');
  },
  mounted() {
    console.log(this.userName);
    
  }
}
</script>

<style scoped>
.three {
  margin: 20px;
  border: 1px solid #aaa;
}
</style>
