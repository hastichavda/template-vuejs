<template>
  <div id="app">
    <my-layout> </my-layout>
  </div>
</template>
<script>
import layout from "./components/Layout.vue";
export default {
  components: {
    "my-layout": layout
  }
};
</script>
<style>
* {
  box-sizing: border-box;
  margin: 0;
}
</style>
