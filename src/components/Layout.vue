<template>
  <div>
    <my-header />
    <my-sidebar />
    <my-content />
  </div>
</template>

<script>
import header from "./Header.vue";
import Sidebar from "./Sidebar.vue";
import Content from "./Content.vue";

export default {
  components: {
    "my-header": header,
    "my-sidebar": Sidebar,
    "my-content": Content
  }
};
</script>

<style></style>