<script lang="ts">
import { defineComponent } from 'vue';
import A01HelloWorld from './components/A01HelloWorld.vue';

export default defineComponent({
  name: 'App',
  components: {
    A01HelloWorld,
  },
});
</script>

<template>
  <img
    alt="Vue logo"
    src="./assets/logo.png"
  >
  <A01HelloWorld :msg="123123" />
</template>

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
