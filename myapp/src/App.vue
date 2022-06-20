<template>
  <div id="app">
    <button @click="onClick('some value', $event)">Click event</button>
  </div>
</template>

<script>

export default {
  name: 'app',
  data: () => ({
  }),
  methods: {
    onClick(val, e) {
      console.log(val, e);
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
