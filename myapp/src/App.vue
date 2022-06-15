<template>
  <div id="app">
    <h1>{{firstName}}</h1>
    <h2>{{num + 2}}</h2>
    <h3>{{num > 1 ? 'number: > 1' : 'Number: < 1'}}</h3>
    <h3>{{obj}}</h3>
    <a :[attrKey]="linkUrl">Link</a>
    <template  v-if="msgIsVisible === 1">
      <div class="message">
       Some message
      </div>
    </template>
    <template  v-else-if="msgIsVisible === 2">
      <div class="message">
        v else message message
      </div>
    </template>
    <template v-else>
      <div class="message">
        Another message
      </div>
    </template>

    <div v-show="isVisibleBlock">
      V show example
    </div>

    <!-- <div class="name-input">
      <label for="joj">Name</label>
      <input id="joj" type="text" placeholder="input-name">
    </div>

    <div class="name-input">
      <label>Nickname</label>
      <input type="text" placeholder="input-name">
    </div> -->
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue'; */

export default {
  name: 'app',
  /*   components: {
    HelloWorld,
  }, */
  data: () => ({
    firstName: 'Andrei',
    num: 2,
    obj: {
      age: 30,
    },
    linkUrl: 'https://google.com',
    attrKey: 'href',
    msgIsVisible: 1,
    isVisibleBlock: true,
  }),
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
