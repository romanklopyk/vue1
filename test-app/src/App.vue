<template>
  <div id="app">
    <appHeader />
    <router-view />
  </div>
</template>

<script>
import appHeader from "@/components/layout/header.vue";

export default {
  components: {
    appHeader,
  },
};
</script>

<style lang="scss">
</style>
