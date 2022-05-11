<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <LearningDashboard></LearningDashboard>
</template>

<script>
import LearningDashboard from "./components/LearningDashboard.vue";

export default {
  name: "App",
  components: {
    LearningDashboard,
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
