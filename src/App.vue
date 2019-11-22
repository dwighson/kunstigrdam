<template>
  <div id="app">
    <Nav></Nav>
    <Landing/>
    <Form/>
  </div>
</template>

<script>
import Landing from "./components/Landing";
import Form from "./components/Form";
import Nav from "./components/Nav";

export default {
  name: "App",
  components: {
    Landing,
    Nav,
    Form
  },
  mounted() {}
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: ; */
  background: black;
  /* margin-top: 60px; */
}
</style>
