<template>
  <div id="app">
    <h4>Parent Component</h4>
    <h5 class="text-xl">Counter: {{ counter }}</h5>
    <button
      class="text-red-200 bg-red-500 rounded-md p-2 mr-4 mt-5 focus:outline-none"
      @click="bgColor = 'bg-red-300'"
    >Make Box Red</button>
    <button
      class="text-green-200 rouned-md p-2 bg-green-500 rounded focus:outline-none"
      @click="bgColor = 'bg-green-300'"
    >Make Box Green</button>
    <SuperComponent id="12" :class="bgColor" @click="test" />
  </div>
</template>

<script>
import SuperComponent from "./components/super-component";
export default {
  name: "App",
  methods: {
    test() {
      this.counter++;
    }
  },
  data: () => ({ counter: 0, bgColor: "" }),
  components: {
    SuperComponent
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
