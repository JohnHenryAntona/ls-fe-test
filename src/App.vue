<template>
  <grid-layout />
</template>

<script>
import GridLayout from "./components/grid-layout.vue";

export default {
  name: "App",
  components: {
    GridLayout,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Gotham Bold, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 100px;
}
</style>
