<template>
  <h1>Component C</h1>
  <h2>User Name by Provide_inject:{{ userName }}</h2>
  <button @click="someFunc">click</button>
</template>

<script>
export default {
  inject: ["userName", "someFunc"],
};
</script>

<style></style>
