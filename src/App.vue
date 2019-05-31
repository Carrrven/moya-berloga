<template>
  <div id="app">
    <img width="25%" src="/img/logo.png">
    <HelloWorld msg="Hello there."/>
    <message/>
    <inputtext></inputtext>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import inputtext from "./components/inputtext";
import message from "./components/message";
export default {
  name: "App",
  components: {
    HelloWorld,
    inputtext,
    message
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #0a1257;
  margin-top: 60px;
}
</style>
