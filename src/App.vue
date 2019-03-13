<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
     <router-view></router-view>
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

<style  lang="scss">
@import './assets/css/base.css';
@import './assets/themes.scss';
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding-bottom: 2em;
}
h2{width: 80%; margin: 0 auto; padding-top: 3em; padding-bottom: 2em; border-bottom: 2px solid rgba(57, 132, 57, .5);}
</style>
