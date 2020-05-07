<template>
  <div id="app">
    <button @click="getChild">触发子组件</button>
    <test-panel ref="panel"/>
    <test-toast ref="toast"/>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  created(){
    console.log(this.$msg)
    console.log(this.$myMethod([1,23,4]))
  },
  methods: {
    getChild () {
      this.$refs.toast.toastPlugin('触发子组件', 1000)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
