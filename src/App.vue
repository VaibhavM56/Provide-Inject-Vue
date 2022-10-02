<template>
  <comp-a />
</template>

<script>
import CompA from "./components/CompA.vue";
export default {
  name: "App",
  components: { CompA },
  data() {
    return {
      userName: "Raju Rastogi",
    };
  },
  methods: {
    parentToChildFunc() {
      console.log("Parent to Child executed");
    },
  },
  provide() {
    return {
      userName: this.userName,
      someFunc: this.parentToChildFunc,
    };
  },
};
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
