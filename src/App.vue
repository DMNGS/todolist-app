<!--<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>-->

<template>
  <div>
    <div>
      <img alt="Vue logo" src="./assets/logo.png">
      <h2>{{ title }}</h2>

      <div class="footer">
        <hr />
        <list-title v-on:onEnter="changeTitle"></list-title>
      </div>
    </div>
  </div>
</template>

<script>
import ListTitle from "./components/ListTitle.vue";

export default {
  name : "app",
  components: {
    ListTitle,
  },
  data() {
    return {
      title: 'My VueJS Todo List',
    };
  },
  methods: {
    changeTitle(text){
      this.title = text;
    }
  }
}
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