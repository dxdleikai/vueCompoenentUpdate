<template>
  <div>
    组件two的兄弟组件TwoBrother
  </div>
</template>

<script>
export default {
  name: 'TwoBrother',
  updated() {
    console.log('component twoBrother update');
  }
}
</script>

<style scoped>

</style>
