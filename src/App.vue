<template>
  <div id="app">
    <MyNumbers
        :numbers="numbers"
        @number-added="numbers.push($event)"
        @number-deleted="numbers.shift()"
    />
    <div class="info-div">
      <h1>State Management Example</h1>
      <p>
        vue-state-example-mynumbers: See article and example at
        <a href="https://medium.com/fullstackio/managing-state-in-vue-js-23a0352b1c87">https://medium.com/fullstackio/managing-state-in-vue-js-23a0352b1c87</a>
      </p>
      <ul>
        <li>node -v: v10.5.0</li>
        <li>npm install -g @vue/cli</li>
        <li>vue create vue-state-example-mynumbers</li>
        <li>cd vue-state-example-mynumbers</li>
        <li>code .</li>
        <li>npm run serve</li>
        <li>create src/components/MyNumbers.vue</li>
        <li>edit src/App.vue</li>
      </ul>
    </div>
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
    };
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
    div.info-div {
      text-align:left;
      border-radius:10px;
      border:1px solid black;
      color:green;
      background-color:papayawhip;
      padding:10px;
    }
</style>
