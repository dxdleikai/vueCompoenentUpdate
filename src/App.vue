<template>
  <div id="app">
    <h4>APP</h4>
    <p>
      app_number = [{{app_number}}] 
      <button @click="appNumberAdd">app_number + 1</button>
    <button @click="modifyProps">更改传递给子组件的props</button></p>
    <div class="two">
      <h4>APP的子组件</h4>
       <TwoBrother  />
      <Two :user-name="userName" @newName="newName"/>
    </div>
  </div>
</template>

<script>
import Two from './components/Two.vue'
import TwoBrother from './components/TwoBrother.vue'

export default {
  name: 'App',
  components: {
    Two,
    TwoBrother
  },
  data() {
    return {
      app_number: 1,
      userName: 'leikai'
    }
  },
  methods: {
    appNumberAdd() {
      this.app_number += 1;
    },
     modifyProps() {
      this.userName = 'gao';
    },
    newName(e) {
      console.log(e);
      
    }
  },
  updated() {
    console.log('component app update');
  }
}
</script>

<style scoped>
#app {
  text-align: center;
  border: 4px solid #000;
  margin: 20px;
}
.two {
  text-align: center;
  border: 2px solid #666;
  margin: 20px;
}
</style>
