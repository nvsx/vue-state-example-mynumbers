<template>
  <div id="app">
    <MyNumbers
        :numbers="numbers"
        @number-added="numbers.push($event)"
        @number-deleted="numbers.shift()"
    />
    <img src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>


<script>
import HelloWorld from './components/HelloWorld.vue'
import MyNumbers from './components/MyNumbers.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,
    MyNumbers
  },
  data() {
    return {
      numbers: [999, 998, 997]
    }
  }
}
</script>


<style scoped>
    #app {
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
    }
</style>
