<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <div class="lelle">
      <Block/>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Block from './components/Block'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Block
  }
};
</script>

<style >
@import './assets/bootstrap/dist/css/bootstrap.min.css';
@import './assets/css/base.css';
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  .contnter{
    width: 100px;
  }
}
</style>
