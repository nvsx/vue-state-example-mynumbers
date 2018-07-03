<template>
  <div class="main">
    <p class="headline">MyNumber component</p>
    <h2>{{ numbers }}</h2>
    <input v-model="number" type="number" />
    <button @click="$emit('number-added', Number(number))">
     Add new number
    </button>
    <div>
        <button @click="$emit('number-deleted')">
            Delete first one
        </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  props: {
    numbers: Array
  },
  data() {
    return {
      number: 0
    };
  }
};
</script>

<style scoped>
p {
    width: 100%;
    text-align:left;
}
div.main {
    border: 1px solid seagreen;
    color: #282828;
    background-color:lightsteelblue;
    padding: 10px;
    border-radius: 10px;
}

</style>
