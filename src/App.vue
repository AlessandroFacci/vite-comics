<script>
import AppHeader from "./components/AppHeader.vue";
import AppContent from "./components/AppContent.vue";

export default {
  data() {
    return {};
  },
  components: { AppHeader, AppContent },
};
</script>

<template>
  <AppHeader></AppHeader>
  <AppContent></AppContent>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
